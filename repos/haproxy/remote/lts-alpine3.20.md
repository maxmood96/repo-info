## `haproxy:lts-alpine3.20`

```console
$ docker pull haproxy@sha256:43a2591a6a62a41dd22edb4452880e9c70de489fbd7c54ffb52d035cccbfe949
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

### `haproxy:lts-alpine3.20` - linux; amd64

```console
$ docker pull haproxy@sha256:2f5e8d19939c2c8e5dbab3e602731e18bd1e7b4b1b6390a016dd4dac59172996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13135631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcaf755b79fb3f2ee7b7ab8a77e44f3b2829123a49cf64b5872258b81f86c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce75fb3e5c0a94c6bc769e958a4eea6b86ee2984495f78ad8f438e3294038586`  
		Last Modified: Thu, 19 Sep 2024 18:58:07 GMT  
		Size: 290.9 KB (290884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279ebe7494b4d509f85aca65128d248bb1ba03fc8115ea15546dba54c52bf95`  
		Last Modified: Thu, 19 Sep 2024 18:58:07 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5e2b7b8afe355bf2ddb5433e7503d44e66f1c06869b41ad2e5544838595c9`  
		Last Modified: Thu, 19 Sep 2024 18:58:07 GMT  
		Size: 9.2 MB (9219490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1b7ab06edbab81e179f4b978da1ce4955612edf4ccc363581d6a7049a361b6`  
		Last Modified: Thu, 19 Sep 2024 18:58:07 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:1e861755174e3f2348f534a206881f785369af0cade676e56899dcbbead28bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4ba70aa966ec272448cd7e4873f8654ff83b9b9d7c11d7eff55ddeac4e47e2`

```dockerfile
```

-	Layers:
	-	`sha256:36d14330be75789290a243af0990bd20c8047c1fc4e0de013d137abf7de12042`  
		Last Modified: Thu, 19 Sep 2024 18:58:07 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea93d9b6b7dc6aae43e89edb9b35bb038b4cdbc3129047865a032842be9e665`  
		Last Modified: Thu, 19 Sep 2024 18:58:07 GMT  
		Size: 20.9 KB (20850 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:fb5a548350fef95bb8eeb35fcc3259fee954f7efe2f6178b59d00788b5275f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12895250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe47a905debe7cee46f5d79cbe0f20b0fcfd8c6f4d89880f6c231ea2953bb0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63be6539ff607f561058227345573d05f1ac17d535fc57da727a82c8d15f5cfa`  
		Last Modified: Sat, 07 Sep 2024 02:33:05 GMT  
		Size: 291.8 KB (291764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4640468ae4017a2fbad0ef7da093746f326843fcce4b7b083ed2ff5847382df1`  
		Last Modified: Sat, 07 Sep 2024 02:33:05 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054e623fa1fda76f2f258128f178dcc71244bea8a8210f992b74f4c092dcfbb9`  
		Last Modified: Thu, 19 Sep 2024 18:58:29 GMT  
		Size: 9.2 MB (9235531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113ee3b7af8c1508c308bcec7425e0abac46266db7ecea8bbd94fadf1654c092`  
		Last Modified: Thu, 19 Sep 2024 18:58:29 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:6776f6eefb37299026de864be90ce44dcaf292b17ae9c388b6f86d69d3250ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e02e689768f032eccf8d4c2aad24e86e1d7b602b1b68ff0d14cd7d562e34553`

```dockerfile
```

-	Layers:
	-	`sha256:1167637150bfaf1ff2c5928628c80f57f756900bf8e00c05de1c95d5b8a90963`  
		Last Modified: Thu, 19 Sep 2024 18:58:29 GMT  
		Size: 20.8 KB (20759 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:eb04e2fa98b8aa19e6390c8faf79ab0b1001424e5fc99285d2047ceb9f1ad893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12472480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c544694e7f58e71b5710804413c66d824badc998c5d4af96c9359a01b2bd0dad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8d6380b7571bdf381f1ba834d2842c0296c2ae63574c4371a79036983f1ab`  
		Last Modified: Sat, 07 Sep 2024 02:47:05 GMT  
		Size: 291.0 KB (290955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5fe183482a6c2f85cb5f99122305b70ec7f474125fa7358bc50f5cec57a56f`  
		Last Modified: Sat, 07 Sep 2024 02:47:05 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a308a7f549fe3fef35212597b7f96ca0daa05e3f934dd55e13923f69089f4b`  
		Last Modified: Thu, 19 Sep 2024 19:01:50 GMT  
		Size: 9.1 MB (9084569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d34f1bd7fa83b0e406f7ac81cbd907b950b3564cb812478d737360928b17f5`  
		Last Modified: Thu, 19 Sep 2024 19:01:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:94c57ca94332f7d8f1254209ede53cc51621b5d48765ecf879b632c5d533b952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9107a9ecb4214fd9a78c75d1470fd6b36f79766b37dc2c3decb14b263161d20`

```dockerfile
```

-	Layers:
	-	`sha256:910620c37a9b35d2726e05b175612afb7c9035e0b8fb9e149d097085fb73ff57`  
		Last Modified: Thu, 19 Sep 2024 19:01:50 GMT  
		Size: 180.1 KB (180074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd878c9f3771b85b13ab206fe87411b106ec70796a28ff8d60536c9506c95c04`  
		Last Modified: Thu, 19 Sep 2024 19:01:50 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e70c62d79067e6d90f8bebe48a18e761287abecfc4005caa8f62c945bf9557ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13613019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7f903d19e76bd3fa7fb5225e33d6acd5eb7f52407eece4858b58831c3e256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475864bf782bde7d14eb4783aae352be0d696ab31c66715603aea9379002a233`  
		Last Modified: Thu, 19 Sep 2024 18:58:32 GMT  
		Size: 293.5 KB (293514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7416df3090c26ab24fc03a74054231b5bd030cc32e2b5a42b2df67838109ad`  
		Last Modified: Thu, 19 Sep 2024 18:58:32 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30152861f1b12421fb8d7c0a79b436b2ec6aa91446de755e0495414553ebb78`  
		Last Modified: Thu, 19 Sep 2024 19:00:10 GMT  
		Size: 9.2 MB (9230407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d330b42260eadbcfa063b83420d1ee0cac222dada8ad0af5ae196dc7d5f16`  
		Last Modified: Thu, 19 Sep 2024 19:00:10 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d83d5e98f56bb1030edd53c6160adff866a9360b20ffa59a7243fb3053b83de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867dd96a1781ca259c85cf621b6004374a0db854f2022f9a4e8a2d59db92bfc6`

```dockerfile
```

-	Layers:
	-	`sha256:1f55dfc88e84b942f63192774779c35770a254e486d7acfbfd08061f72160457`  
		Last Modified: Thu, 19 Sep 2024 19:00:10 GMT  
		Size: 180.1 KB (180110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a369e754f5610410e308e1f1fb7f98337426802a8104ed3d802c34b1dbbbaa7`  
		Last Modified: Thu, 19 Sep 2024 19:00:10 GMT  
		Size: 21.2 KB (21198 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; 386

```console
$ docker pull haproxy@sha256:298ad5fa6f6857ae50f47156555f1583ce3b163478b9f578f02df6c4d9872d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12773248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1725b58bedfec70b705941714ea91dfa3da9ad751bfa205f34c3e8bcf8d4b296`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d91303d5cd27e1865e17317ac3b8447618060203c164265135e8c62b0a4dc9`  
		Last Modified: Thu, 19 Sep 2024 18:58:19 GMT  
		Size: 291.4 KB (291362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264999afc41c3ffb30f42ff1dc70fc6a0fec16a807751baf0b42803c37b1a1f4`  
		Last Modified: Thu, 19 Sep 2024 18:58:19 GMT  
		Size: 977.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85208d36ee44e00fdb4bd0991491f17cebf98ad74aab1f7c04253f7b4d8123b`  
		Last Modified: Thu, 19 Sep 2024 18:58:19 GMT  
		Size: 9.0 MB (9011270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b20a072b2a35f1878941050052de9813fa601773d9dda35385558800d110c`  
		Last Modified: Thu, 19 Sep 2024 18:58:19 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:7aa568f235e23e7f59fe4214f4d74dcc6525331f0d2d965aff7f19ab84e2844d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44228b472aa83f34a80ef9c8555aaddfa564f82f45d0bca58db21b0b43a8345a`

```dockerfile
```

-	Layers:
	-	`sha256:f6562c76027dd99264b87419a14093b7163eb124ebe236a26fe6f369dfc056aa`  
		Last Modified: Thu, 19 Sep 2024 18:58:19 GMT  
		Size: 3.5 KB (3488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc2be1b8f8da82fa27661ca39111be7f0d6bce212c556b6570800f21002b392`  
		Last Modified: Thu, 19 Sep 2024 18:58:19 GMT  
		Size: 20.8 KB (20797 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; ppc64le

```console
$ docker pull haproxy@sha256:385f05cbf48c8f58846991e8c95bca573cda976acda5ffb5d03692b9396370f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13619666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23e73f207aa0098f247adc513c619a75c3b8e71445f46af09672743984f9c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb2e8b56632336aa0310ede33c6fd323035c958abd85d5d5e04f5a71003ea97`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 294.0 KB (294037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9303b3dbb55b7c4ae69878d5171343cbcf55be490ec2f722992e88711a125cb9`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a5b7d7e8bb5642ffb635a44a021c3f80f69959ca739584be8373cc70523169`  
		Last Modified: Thu, 19 Sep 2024 19:02:39 GMT  
		Size: 9.8 MB (9751757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878f185dfec1416416225c326b632d2eba4da307cd2b08c11e88e9673e8016aa`  
		Last Modified: Thu, 19 Sep 2024 19:02:38 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ee65215e4fdc7d1921e7a7a0eb9307c41621a0ffb0b7337655ce37042501829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (199025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933ce8e3167ca69c43ce14a3187eac5ecf8023cc67b58a3810ee40d53b61c91c`

```dockerfile
```

-	Layers:
	-	`sha256:f6bd9fc67e5414c8ce616891306880d505e533fbae0fbe5807c6dd1e80e26056`  
		Last Modified: Thu, 19 Sep 2024 19:02:38 GMT  
		Size: 178.1 KB (178110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e89dfbc447211cfb4b5d177c0c38fbeb1e114a01f8c9621c24e11f2092e83a`  
		Last Modified: Thu, 19 Sep 2024 19:02:38 GMT  
		Size: 20.9 KB (20915 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; riscv64

```console
$ docker pull haproxy@sha256:ddad9b63032de8b434198cf16bf22e69513af549f069c68e3a9c956a58b9108e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12576743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80046df2b6492d77a22423bc9ead9b253168c67dd9331e7d22418e53c3237f27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912bcc9b9311dac341d2f9998e7f1fbd54b6e8e36f756419b6bbd5e959954759`  
		Last Modified: Sat, 07 Sep 2024 19:05:06 GMT  
		Size: 291.7 KB (291669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6038f190563add9bb61aef08e82a177b286f8f88aa0fd81e4b22e6ba042a38`  
		Last Modified: Sat, 07 Sep 2024 19:05:06 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c0df5f278325d953fd951d14524402378d7a0ec551743d8b723f4d5aa758b`  
		Last Modified: Thu, 19 Sep 2024 19:31:35 GMT  
		Size: 8.9 MB (8912165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c342e958c9449c99111486445641d7961246346a6e427b8f429c7557c4d40539`  
		Last Modified: Thu, 19 Sep 2024 19:31:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:8e12f4ed67aa9c637ae818ce1aae3d850a16f2d6daed0b2525c8a7ec1362cbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (199022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abddefd6968c829ec8856180099f93e0befc7e37b609c581158ad50cdb77a8f0`

```dockerfile
```

-	Layers:
	-	`sha256:c70b6ef60b4256465f0584238ed61f10f6fb6a2aa09130aac1599908fb425310`  
		Last Modified: Thu, 19 Sep 2024 19:31:34 GMT  
		Size: 178.1 KB (178106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1ac333fc8f789e2221065d0d44a2d50b7870db4a0666c7506e2168e5349f43`  
		Last Modified: Thu, 19 Sep 2024 19:31:34 GMT  
		Size: 20.9 KB (20916 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; s390x

```console
$ docker pull haproxy@sha256:621bd6307bfac84a8c5682cdfa111af981299989d7736df392c7beba12ad3c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13214301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f074f382fa8a8e29dceffcebe9356ee661c1f0593ea43af1b85b15cb360d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09cecab38a538b00144752b5409154091d2a1c1ee0cc68caec4e9ca682fc59`  
		Last Modified: Thu, 19 Sep 2024 18:59:32 GMT  
		Size: 291.9 KB (291899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0e9c31ea21575aa8eaa08d8f7a2d3c205b1559169e3a7684a814bb3b34413f`  
		Last Modified: Thu, 19 Sep 2024 18:59:32 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae0dae1ed8c199744a571d163d4829e60d133a141dc57a890e82992eb8328e3`  
		Last Modified: Thu, 19 Sep 2024 19:02:24 GMT  
		Size: 9.5 MB (9459353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa2aaad9169d59873078ea3cd9a6c49729b4c4018eae00969c41f90f0bcc7f`  
		Last Modified: Thu, 19 Sep 2024 19:02:24 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:391dc6052801a2a8d7bce9cc65d658f8ab255f326856cb656a8b0170d7b1700c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 KB (198901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd065a17d9bc68a20740d3567db815335482aa6caf1626b2b668447d52b5799a`

```dockerfile
```

-	Layers:
	-	`sha256:d48e93d0b54abff75487dccd080a1430bad404cd036a1bf57a49a40a5882eb00`  
		Last Modified: Thu, 19 Sep 2024 19:02:24 GMT  
		Size: 178.1 KB (178052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b45e61d75addd80a4eca5f0a4ea65326ac86e58035efe477a5941484bcad2a0`  
		Last Modified: Thu, 19 Sep 2024 19:02:24 GMT  
		Size: 20.8 KB (20849 bytes)  
		MIME: application/vnd.in-toto+json
