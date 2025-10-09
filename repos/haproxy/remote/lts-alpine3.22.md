## `haproxy:lts-alpine3.22`

```console
$ docker pull haproxy@sha256:2e182f09427e8962986332bbcf29e9e6bd4d3741d9318f1823373ff0ec17e514
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
$ docker pull haproxy@sha256:a3aef6938ce23cea8d86d15965336bda264da5e42302e5653d0e97e5d0688f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15139109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3e8cf6a18ca82ce959cda4ae0344575137a64f86d95a2b449ed39424d7f8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c0654f77bf14303544b2aca1dfb78f048faea9304322f408914cd65443bed2`  
		Last Modified: Wed, 08 Oct 2025 22:37:23 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236a0d9ac9b02b63f7605fbbfe81bb569b472c4fc3b5e82069cce9c62e539f82`  
		Last Modified: Wed, 08 Oct 2025 22:37:23 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5dab160d04d56432dc8c99f5c2dfd436930263bc4f00df5847e2fa275cad48`  
		Last Modified: Wed, 08 Oct 2025 22:37:24 GMT  
		Size: 11.0 MB (11044071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3edde546a4f04c7273d0af3d44587bfc408bce8639fa5a29c7da44a02bbb0`  
		Last Modified: Wed, 08 Oct 2025 22:37:23 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:075eaf0fac94abb3b8e93aa9f57e2e11fc0212129959f8b494b661f7ec9d249d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 KB (208467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413dfdd4b044bc64d959d2683db7d6436ac0d44caac905c647a3e653a28a85af`

```dockerfile
```

-	Layers:
	-	`sha256:fdae9be487368748feca2ea855c642badb1cba71a67c5c806c068dad230a6d34`  
		Last Modified: Thu, 09 Oct 2025 00:58:04 GMT  
		Size: 187.6 KB (187581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f619ace909587e608f8767fd59a77f30c2456f96a673cd867d8ed370f3b28184`  
		Last Modified: Thu, 09 Oct 2025 00:58:04 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:4287fa19913accf2dfa0f4c329599653976f40f0f1584dbbbb0dbb8c244cfb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14935175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0eb7b8794fb9c974a1c8abb86cff6f46b8c83053679e628624f99fd785ea4f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79aaaf84ee6b842b08ddec87a986e9b81c451bd17c6b9ed215c12bffee69b36`  
		Last Modified: Wed, 08 Oct 2025 21:40:21 GMT  
		Size: 292.3 KB (292312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8619ef1ed252cb7b32f305f47bc371b909141a263b43b46c33d9f40c283da2d6`  
		Last Modified: Wed, 08 Oct 2025 21:40:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c328d3b7a75d0fd6329fc41af6c295f8e7a6390138ffd08b8521095f0f6599fd`  
		Last Modified: Wed, 08 Oct 2025 21:40:22 GMT  
		Size: 11.1 MB (11137346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85983a2373906f981a72145a1905b53533823fd47008012ec09b2a4501167bc0`  
		Last Modified: Wed, 08 Oct 2025 21:40:20 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:358e3890485251f3026473ef6b8677497763a472b25400c9ebdbd089ac783d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b36a68e31689456c3348ca64edeaffc07d50c947658625cee6da9063a86a6c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f7c3e6fdbba2418ea5bd3c2fc0f7290e3d9ac8083de3b9b70c8ddc0f170ab9f`  
		Last Modified: Thu, 09 Oct 2025 00:58:08 GMT  
		Size: 20.8 KB (20810 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f19f7ab17883e2ef805fe24c00b3d6fe83e4c59617f4bfef5d67368c3a7e76d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14483183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f43af01adbbf8804b217ac4dc93b56e17237466c4ef4ef9d44f285043918e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0db136ed1ba0ef7db0a6afb21acdb38a8a712bf81e3da40d22ab525bd0665f`  
		Last Modified: Wed, 08 Oct 2025 21:17:11 GMT  
		Size: 291.2 KB (291210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef179efdf6180c9e2d5c44588f673ae17659725a0add9026c849148c4f13186`  
		Last Modified: Wed, 08 Oct 2025 21:17:11 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ef0019c9b639d9cf4094fe835d6a3d95422c38ab83fc758e2167f58502564e`  
		Last Modified: Wed, 08 Oct 2025 21:17:17 GMT  
		Size: 11.0 MB (10968978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aa0ee3954c41bd5cf9344d5ca7fa951ba3e8448e0610bc3c6e9dd65ad3f05a`  
		Last Modified: Wed, 08 Oct 2025 21:17:11 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:b7523979a9a3ae1bc1fd65f52bd77421daaeb4f144edf798370bac30f4879591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 KB (208674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7838b07f608b7cc3ae2d1680b0ba62e4edc8b887720fa394a517f69d63a49a`

```dockerfile
```

-	Layers:
	-	`sha256:eec152f6793d47f0f53725eabca8fedec5a5d1f8a6aa0aebcf9a9d5c81b7cb48`  
		Last Modified: Thu, 09 Oct 2025 00:58:11 GMT  
		Size: 187.6 KB (187649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9f8bf40865eb57cf305658e9db22ef6871a4bf56dc313af730b1e961d99057`  
		Last Modified: Thu, 09 Oct 2025 00:58:12 GMT  
		Size: 21.0 KB (21025 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:eb52f85553ccb67e88c8019f6c7003931943afd5170dbb6cab34f837007410dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15416224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0c34dbc936902d6f9c95588de26ae49c83e6c127a2fd7d98c42b065a3feaf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58729f773b2aaa8540c99d1b956db11355c44a299e8a43f3fe4d32e33a9dc53`  
		Last Modified: Wed, 08 Oct 2025 22:20:30 GMT  
		Size: 294.1 KB (294089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aab9d81b74f0187c16cc4973758b8d3b655d362874e1ec395412f6e9c9bbc5`  
		Last Modified: Wed, 08 Oct 2025 22:20:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c2cabea18469af189d76f7a1e9976e21973f14bd356fd36555fa573469bc37`  
		Last Modified: Wed, 08 Oct 2025 21:28:05 GMT  
		Size: 11.0 MB (10982628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38aef6571c7dadd3198cde50760decca0fc3be997207961aebaa5eb663cb3e5`  
		Last Modified: Wed, 08 Oct 2025 21:28:04 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:5d31dc6c6c8e610b0f1de65deebfa1ac8e62a05d98bb34d19d1c0caf59860530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 KB (208754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff19b08adfe42c8b62c4b3c6e1203cfcfc3d8bf27a4251edb2826e6277f8b21`

```dockerfile
```

-	Layers:
	-	`sha256:706204d1d8db4cea0f9253f7c8be3483767c3088c5297b4293d3ce94951effe0`  
		Last Modified: Thu, 09 Oct 2025 00:58:15 GMT  
		Size: 187.7 KB (187685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36e404bcdc8dc74e5d187a67e34817f32a43b92a6d9c49edc481ea288f048cc`  
		Last Modified: Thu, 09 Oct 2025 00:58:16 GMT  
		Size: 21.1 KB (21069 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; 386

```console
$ docker pull haproxy@sha256:0b52e25681c327acb9aadeb7de484aeb9bb972721ef5a100975a77f617c4a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14682337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fbc67b3f58aba2f7fcf478f6ec928ddd1ee7aa284285b531c5472da11ff354`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc83eb0e8b2bc7605e06f4a9da1527752fea9f051e8f9cddf36101bfc81661`  
		Last Modified: Wed, 08 Oct 2025 21:14:15 GMT  
		Size: 291.6 KB (291624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f82c86ab0185eae02e3995892335cb54e7deec2fc79c818c74be5eeb7f756`  
		Last Modified: Wed, 08 Oct 2025 21:14:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73f126a0128a5145f59881a0ed47f5e94fb960b1c3274811b2a24eaf228513`  
		Last Modified: Wed, 08 Oct 2025 21:14:17 GMT  
		Size: 10.8 MB (10770345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3526c21ac36567f80d7eb5bb929efc7c66b4ebe93d75acdbc69c3b20528fc2f6`  
		Last Modified: Wed, 08 Oct 2025 21:14:16 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:8144dfde2f213f720f35e762c30e0ae472650a3a0af9c892b710c013702e62c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 KB (208367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6e847994f9ec825661307b6c4a7e30299b1f87f2299055bb1e55e14cf03915`

```dockerfile
```

-	Layers:
	-	`sha256:2c0e2d7ffdc9b21b2b06cf94bb8151fd2c5988de7b93a82ba3359d0a7b25e6f3`  
		Last Modified: Wed, 08 Oct 2025 21:56:23 GMT  
		Size: 187.5 KB (187536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4712972f6bb32024a63f40fd48ee500633cbd3919c8a0469c6fd386c45e46f74`  
		Last Modified: Wed, 08 Oct 2025 21:56:24 GMT  
		Size: 20.8 KB (20831 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1a3131b417a10f7a7c6c3bf4c25dc991e8bb3dd38c60c92c0b65b3080c4ea1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18140139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf8b4273166236c18fea7c1bac367b794edd30eab992c119e46639519875067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8732dec6cd543e401e26e214c4c77ec3dee44b995d51b60cbc3b80fc6b5b7b5`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 294.6 KB (294629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41efe5ccdbe71c63281e775f25396cf39efc8ad7483b30056ab71e3744bc55`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b302c8f3f70fd6d7d607cbe458ef0d36aeb3acad1d39820d40de5924b3fc2b13`  
		Last Modified: Fri, 03 Oct 2025 18:34:00 GMT  
		Size: 14.1 MB (14116958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f7d14897b557f69e5b35619ad4d2c6fb4e586a5dbd20d5eee31c2c4e68bb14`  
		Last Modified: Fri, 03 Oct 2025 18:34:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:cafa3d4c3f65c173882c32a2db21418292f54dce921f481feefb773461a22e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 KB (207730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492a8cd7afa9e8bd6c8d9a4cf4efa8b4241c3f8ecca1509fa546cfe650f61574`

```dockerfile
```

-	Layers:
	-	`sha256:7e75bde25d027e4b0a457b442c6202dd0b8f914528c7e1ab2fb3ceb5b9edb5d6`  
		Last Modified: Fri, 03 Oct 2025 22:02:01 GMT  
		Size: 186.8 KB (186771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b002b17fec91a0917670a6080481fedd3804b5a690957ab2c52d166fbfd95f`  
		Last Modified: Fri, 03 Oct 2025 22:02:02 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; riscv64

```console
$ docker pull haproxy@sha256:7ce6763edb37ceab62ccdcd93971674af5995fcb4fa3e908bda609f8547db135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16806515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502fb5030217387e953fb653a44fb0d385b50eee7488e940b4b5d760ca7dc341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79712820f0452a123addbfb91430270b0d001316864ae62a55a037e537ae841e`  
		Last Modified: Sat, 04 Oct 2025 07:16:48 GMT  
		Size: 291.6 KB (291554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d782534a4949407f13c010c96e86bdc0c3ee74424633c0064803e23de2a7e8c5`  
		Last Modified: Sat, 04 Oct 2025 07:16:52 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddad5bd4e73cb25965adcaf143d47470ff1229e73eacd6cbb1110d0bfe27a427`  
		Last Modified: Sat, 04 Oct 2025 07:14:24 GMT  
		Size: 13.0 MB (13000713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da79dba50100a40201d5c424a91433860d937a0571ad20e05b1a130df9bb481`  
		Last Modified: Sat, 04 Oct 2025 07:14:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:2d6aa991dbbf84ff06a62e53c81328d4d9499a3630eb15288cd434c9b51f0f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 KB (207726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36015c6f400f26b882948cae693696565343a254011266fefd0faf4d940608cd`

```dockerfile
```

-	Layers:
	-	`sha256:7aeb1905bde98995a6336fd609229987299da035d291f584c416ec9494b9d19c`  
		Last Modified: Sat, 04 Oct 2025 09:58:07 GMT  
		Size: 186.8 KB (186767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baafbb2c3a86fa63dfd47e37ab8d7c69ec1b487447cda9ff8c84b27b23ac48a2`  
		Last Modified: Sat, 04 Oct 2025 09:58:08 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; s390x

```console
$ docker pull haproxy@sha256:d8d64c68b922825f36cb7109f648c9ffa114daf3070155852e0f3fab736606a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17714650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42521b17baf5af81c01c9a553316b921ba22ed154e44ab4abbd26dc7805fcfdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbb9ed5d056774b0f6fdde4aa100dbf4765f9ac187950a0e9742d065c307fb3`  
		Last Modified: Fri, 03 Oct 2025 18:30:09 GMT  
		Size: 292.2 KB (292191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0feeaf75f6a418852418391369c7b138f0a9223b2a4a67c5b29f6c1ac5b589b`  
		Last Modified: Fri, 03 Oct 2025 18:30:10 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63793f4ae120e7fe8ad35891af07c1458b24d3b1d95166bfab4abf0e0e5dc2cf`  
		Last Modified: Fri, 03 Oct 2025 18:33:02 GMT  
		Size: 13.8 MB (13776046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b751f9f533dc74ba15d2b4d998272b066119d01865b43cee3e1376c359bf77`  
		Last Modified: Fri, 03 Oct 2025 18:33:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:ab9c8971e73699ea6518511e465cb1d93e38d4736244c7f9ff148f76d72f67a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 KB (207599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb58833a36696f7939ef9c5dc51a3b15907f03d0c4e24fd464db4978a81a80d6`

```dockerfile
```

-	Layers:
	-	`sha256:85c184e52baa3218501345da7b0fbdabf97e8e5942326fbb8da81bbc9fc1dad5`  
		Last Modified: Fri, 03 Oct 2025 22:02:08 GMT  
		Size: 186.7 KB (186713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e467214e85cd8f1e4bc9003956b195fb877b3f596acf9701fdc59bd42b1d832`  
		Last Modified: Fri, 03 Oct 2025 22:02:08 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
