## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:9143d645e5b526b8f1275aa092c4fabfd779d8cbbd3f28182c979b428cf23536
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
$ docker pull haproxy@sha256:b014f919a38cb02d89794282e8c6b63abe87457a3309fa9f8976c0fb5d071376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e35f0bf30df09bb16b14c5c1d64e7ce1015f2178c99e3d9739edcc91ed91e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:27:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:28:27 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:28:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:28:27 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:28:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:28:27 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:28:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:27 GMT
USER haproxy
# Thu, 18 Dec 2025 00:28:27 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:28:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a70bc20cd908b4bdcf72c039fd58e516adf7e3154c27f16aafcb3bf18acd232`  
		Last Modified: Thu, 18 Dec 2025 00:28:40 GMT  
		Size: 829.6 KB (829636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464d6dba2a338298a9117728d1867d1570cb59d9950de99759f1c39cd4380648`  
		Last Modified: Thu, 18 Dec 2025 00:28:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8042c4a527a856f8f3d4cc289d4373c733c8a1b7cb0abd34a4a6a577b3fe93d`  
		Last Modified: Thu, 18 Dec 2025 00:28:43 GMT  
		Size: 11.1 MB (11109344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4a2efdd6927fd534e31c0d29feb164dcd255bd92290841536c9a422e4610b`  
		Last Modified: Thu, 18 Dec 2025 00:28:40 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:fe5c9a0ad66128d125bd7fdf67d509a1a8800fedf4d4ca105f01f2ef2400d61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb3fe05f47aedccc5341488d11c93240f3e56fc5534e07a300c831986b7f5e1`

```dockerfile
```

-	Layers:
	-	`sha256:1e17c1996f2a96478938450a56347914952a82056c46cf7b1111cc009364d4e2`  
		Last Modified: Thu, 18 Dec 2025 01:59:48 GMT  
		Size: 227.3 KB (227322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b142f204f7a19628dbc600f85bdd46852e6d79717f3b0681bfa5358afc3ea49a`  
		Last Modified: Thu, 18 Dec 2025 01:59:49 GMT  
		Size: 20.4 KB (20448 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:c82cb8484d5fa739195ab054bb22823f0e6c782c50c980e046500bfca37f1aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15607033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a4aeaa7e6548d4d351ec9005d79870244acead40162396f587c4bbf767e8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:28:55 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:29:31 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:29:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:29:31 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:29:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:29:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:29:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:29:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:31 GMT
USER haproxy
# Thu, 18 Dec 2025 00:29:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:29:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2aefc877ffb3d4204a1a5131b2643b39d6f8b7fbccf1e15c8da7a73d426f51`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 821.9 KB (821852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dabe0659afce4f0fd490117901eeba2ae49399ca58db2f9235334bf89f55517`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fefeef9f294b49ad980b6dadb9e1aa77b8773591f66f2830e50754f9fdb6c3`  
		Last Modified: Thu, 18 Dec 2025 00:29:44 GMT  
		Size: 11.2 MB (11215315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195844b05e45f1ef5bcdb37124420294d1ea17adb1ce70a8c192b118455c4c8d`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:070a53cdc1b2eaae61760f30bbe34a0e2d97973675165681d6097955f37914bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02cc74698455e1276f5e25b6436df1403f5ec1fdd070c78dd928761ffbfc6c7`

```dockerfile
```

-	Layers:
	-	`sha256:1dfe4ae6ff5583c8b516a9435c95b14b43f7ad16df5aca5cf5aeb48b847daf65`  
		Last Modified: Thu, 18 Dec 2025 01:59:53 GMT  
		Size: 20.4 KB (20355 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:4c81b2a498f46629de95be4711aa88938d438d0fc76f91e8a0be9dd0610edfa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb89c5522cfe45547075981f9b5bc98ed1cc6dc00c83c25cf3040fbf651b384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:30:10 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:30:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:30:10 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:30:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:30:10 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:30:10 GMT
USER haproxy
# Thu, 18 Dec 2025 00:30:10 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:30:10 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db43f986b959f9e64ebdeb1f30079fefad656f94feef783689b08ea394975195`  
		Last Modified: Thu, 18 Dec 2025 00:30:22 GMT  
		Size: 777.7 KB (777721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c1a4e43d1f5f076663a44682100babf552f0f37ca90c5459c9184857b8fd55`  
		Last Modified: Thu, 18 Dec 2025 00:30:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d012471377d7f4abea94ad3d252762de07860c80e7c4efd094cdeb5d240a906`  
		Last Modified: Thu, 18 Dec 2025 00:30:30 GMT  
		Size: 11.0 MB (11048811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c1d2318f2b561fc0c958fbb6ba521e270c2f3a7b8fbbb2efa94ec685a8a7b6`  
		Last Modified: Thu, 18 Dec 2025 00:30:22 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:de6420c2018e7c8e44abf0f0f2f1d131f2c248e7a86e9ca1ba7be9c6f550e858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 KB (247294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6248c35ec6b66aaa4bc523c3b338b080ceae28d00d4aeec8327df197522eafb`

```dockerfile
```

-	Layers:
	-	`sha256:f74b273e7890f3f67f60b8e4627352a364c3f96278a48559976deb943b78b3ed`  
		Last Modified: Thu, 18 Dec 2025 01:59:59 GMT  
		Size: 226.7 KB (226724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab5ad604d6dc86a3f8a1bc3b73dfa47d7666180e54235b7125b73a325eeb2bbc`  
		Last Modified: Thu, 18 Dec 2025 01:59:59 GMT  
		Size: 20.6 KB (20570 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:cbcceec762f75d7039733ed1362fffe86421267541369256f1baf39839b1c101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16003912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f9a4c66fecd172582426f32759a7e0fa0e658f625e44af967b3e37b6c03ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:26:54 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:27:25 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:27:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:27:25 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:27:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:27:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:27:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:27:25 GMT
USER haproxy
# Thu, 18 Dec 2025 00:27:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:27:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196872fa9e59f357053181c7997a953dcf0e0b9db96415cb2df3c313abf9b2a5`  
		Last Modified: Thu, 18 Dec 2025 00:27:39 GMT  
		Size: 842.4 KB (842351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf4e09d787ce18165b806580a25265ba9ae70f35dbc015104d4c00a95e03969`  
		Last Modified: Thu, 18 Dec 2025 00:27:39 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78d285e3eee97740b85934b4cca7ba19e5bcf1f8c4ef999680e9e817929114e`  
		Last Modified: Thu, 18 Dec 2025 00:27:40 GMT  
		Size: 11.0 MB (10964385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bf268705fe16e2fdecb2bd7f76c75a5c08192579859309f84d6eb3db37a0d0`  
		Last Modified: Thu, 18 Dec 2025 00:27:39 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d717c0460ed1b7c94a6cf2ecf6322f6a0567b9f7b9b18a74b040848a2ee7087c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 KB (247358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4da1b22f898341cc564a53507f1d6404c914e71cc32ee4c6f4fb5b03f2ed4`

```dockerfile
```

-	Layers:
	-	`sha256:64a2147fc5326082dcc9f57ffcfaa3d8a204492d58d8573fa453b2d3ae427347`  
		Last Modified: Thu, 18 Dec 2025 02:00:07 GMT  
		Size: 226.8 KB (226752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60a8769aa93115f6242ed3e7dd003238d6676da1de7160aa09aa859b4bf0ead6`  
		Last Modified: Thu, 18 Dec 2025 02:00:08 GMT  
		Size: 20.6 KB (20606 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:a43b4fe77c1daba95773af428ca26d7e5f460736d3cdf7fd1a4ac5d8e5993de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15342163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c239bf71748e1bf40b55c60973ebb0ae669cf79158a36b3df25006e2582f9df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:29:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:29:55 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:29:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:29:55 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:29:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:29:55 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:29:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:55 GMT
USER haproxy
# Thu, 18 Dec 2025 00:29:55 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:29:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3148b066188f1bb03422115383aa779eb3cb70d636b6ea9e6c4cd951cd5364`  
		Last Modified: Thu, 18 Dec 2025 00:30:09 GMT  
		Size: 835.9 KB (835939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a30957bdf0e700b2648ff2fb20280db052dd0f58bb4ac6dcf347f2f1f0116c1`  
		Last Modified: Thu, 18 Dec 2025 00:30:09 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b9372e217e979a9df24af9fb5cfcac82d367356bab40813dbcb06a6afc809`  
		Last Modified: Thu, 18 Dec 2025 00:30:09 GMT  
		Size: 10.8 MB (10818689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f660025a045a190b17fa40a1372843bbc08454c2c7e923233882bd2c3731a4a`  
		Last Modified: Thu, 18 Dec 2025 00:30:09 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:caa96342146abc414d5a3ff97a2c132fb75c736862838530dcebf33ffbd9055a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 KB (247689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66920ca46f78c19832fc732508d07dd98fd81dd6245fef7ff85cde900f397c3a`

```dockerfile
```

-	Layers:
	-	`sha256:ee184f4ac4ba660950350ab63976491fcaa64c9824e99d4b341a215870a19d60`  
		Last Modified: Thu, 18 Dec 2025 02:00:14 GMT  
		Size: 227.3 KB (227287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077b3cb251739a0dd4ebf8d6d9c921f0fdd7cec2b10f69249e3f096207286a12`  
		Last Modified: Thu, 18 Dec 2025 02:00:15 GMT  
		Size: 20.4 KB (20402 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:b902e6f49a9a5c6bb18bf3591e5eb727a29d2b7ef7424d3b0523d61173d935d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16509577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc9badc98e18574d8e716825112b91ef0ac55527fe7b1461662a36bdf5aafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:27:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:29:33 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:29:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:29:33 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:29:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:29:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:29:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
USER haproxy
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a0fdc4bb301c69fecfecf50058cde63750c19fa0b3a70fa341b6f2fcf528f`  
		Last Modified: Thu, 18 Dec 2025 00:28:33 GMT  
		Size: 865.8 KB (865810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00141f74db030864fe82dfb8884aeee311a70a3e2d18b678d14d71fcb989fdad`  
		Last Modified: Thu, 18 Dec 2025 00:28:33 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7818ed6bce694afe93726b8eac6b0baefed498fc3368dad14817769455dfd3a0`  
		Last Modified: Thu, 18 Dec 2025 00:30:02 GMT  
		Size: 11.8 MB (11814573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ec83d4fbe4f7c068b023f429edd5c6d5474260fed303f110692129be467205`  
		Last Modified: Thu, 18 Dec 2025 00:30:01 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:1a10222433170097725ed56200a941c28145929f73ee3dfcf5c022cc12c56d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac2cc5cd6ac42bfb2bbcfec8f38c18242e1a2776f01390a7d24ed2fd10347c2`

```dockerfile
```

-	Layers:
	-	`sha256:8ec9f45f5c2f42e4e91f66c436dff9a0819dcfaedb9b0e8bfcbc430648050c6f`  
		Last Modified: Thu, 18 Dec 2025 02:00:19 GMT  
		Size: 226.7 KB (226717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa16d197074e54aca3adb5f8dfcf91fa7153c8a532495f37510157fb01b61e30`  
		Last Modified: Thu, 18 Dec 2025 02:00:20 GMT  
		Size: 20.5 KB (20508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:a7e1b42e50fd5974b6a1643b18ecb4e3ac91383a06838a63eb05ba44017d02f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16441768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066dba492bf0f9a222ed506d385647d53344be89a13409c03e682dfbdb411035`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:58:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 23:58:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 05 Dec 2025 00:51:25 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 05 Dec 2025 00:51:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 05 Dec 2025 00:51:25 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 05 Dec 2025 00:51:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 05 Dec 2025 00:51:25 GMT
STOPSIGNAL SIGUSR1
# Fri, 05 Dec 2025 00:51:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 00:51:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 00:51:25 GMT
USER haproxy
# Fri, 05 Dec 2025 00:51:25 GMT
WORKDIR /var/lib/haproxy
# Fri, 05 Dec 2025 00:51:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041d7e63bf492044141027bbaf934a4aac2207f5ddd4e7faa96471d04cee567`  
		Last Modified: Fri, 05 Dec 2025 00:12:40 GMT  
		Size: 849.9 KB (849928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbba9fbf73e4fa52ee2072e401626a941639ca7e5a46640a758816b496412e9e`  
		Last Modified: Fri, 05 Dec 2025 00:12:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1282a7af1c40ded34bac1ade487f5e0174684d198dd2ea26a22af31d15cef18`  
		Last Modified: Fri, 05 Dec 2025 00:52:10 GMT  
		Size: 12.0 MB (12006877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbb1d3e9f1ffdcd6fd81b387e4f93d05d10d48e168f0d8e8ed2c06fb4ee1179`  
		Last Modified: Fri, 05 Dec 2025 00:52:09 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:6a8142e8cb8fd1651323db6bcdbee9bdd04231e904729a331f23b8d44c6ccec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b8d15cc99e2f43287e179c587fd20dbe080e7b31ded87663787312716a1a08`

```dockerfile
```

-	Layers:
	-	`sha256:9e49baff0715047e558783795a412650b2f7cb79c601e19caafb68ef0b8b4517`  
		Last Modified: Fri, 05 Dec 2025 01:57:31 GMT  
		Size: 226.7 KB (226713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feec47965f9a62fa06e65e80bc443cfb82f939aa82ddb11f18a7b80821c811bd`  
		Last Modified: Fri, 05 Dec 2025 01:57:31 GMT  
		Size: 20.5 KB (20508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:674eaf56ce29331d7361de10f8719ae04adc945b90e4c336ae949a65815800bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16048519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3907d3808bcb79354bf478e4c1e0753358d282758f924ed1808d02f32269346f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:26:23 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 00:28:22 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:28:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 18 Dec 2025 00:28:22 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 18 Dec 2025 00:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 00:28:22 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 00:28:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:22 GMT
USER haproxy
# Thu, 18 Dec 2025 00:28:23 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 00:28:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d72f959e55ce0a0ba7077382dc97d683e56c7d1901d55abcae919e934370a`  
		Last Modified: Thu, 18 Dec 2025 00:27:32 GMT  
		Size: 891.5 KB (891544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c5385c88d82e1ab96c9fcdcd46f6cfdcff7ab2a864621ca280f82cbc067465`  
		Last Modified: Thu, 18 Dec 2025 00:27:32 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ceafa033d83f3a7af852c521972acd17ba0490678e205c9f54b460a6f725ff`  
		Last Modified: Thu, 18 Dec 2025 00:28:40 GMT  
		Size: 11.4 MB (11431230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea8c1fef5b557ffcdc2698d909cb7142569c612b96b65ac157d0c92732bc941`  
		Last Modified: Thu, 18 Dec 2025 00:28:40 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:4a2b544d129fa4a703d6783827a33eb3f6498bd282402f3d3a785791fc03eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 KB (247119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fce5fe83ca67ece3e60f92b9be9fc199deaa3cd5404a923715e6cc6ae08026d`

```dockerfile
```

-	Layers:
	-	`sha256:8417609def72173be439a0b64543a4d283d262b844f0c656bd94d7e2078c06b8`  
		Last Modified: Thu, 18 Dec 2025 02:00:27 GMT  
		Size: 226.7 KB (226671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aee7ebe08e57c91271539f6938dca13d7ff7cdebd5288aac9df6a63e596c72`  
		Last Modified: Thu, 18 Dec 2025 02:00:28 GMT  
		Size: 20.4 KB (20448 bytes)  
		MIME: application/vnd.in-toto+json
