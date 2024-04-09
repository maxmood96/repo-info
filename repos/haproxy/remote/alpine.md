## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:d3d2bd535a23d9d35da37f4c3d5d2d23c7851a885a69e6f966525808926e1a34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:f046407028ff07407f82f846e677dc3c2a622b49a7fca70d748bec0b236e24fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12306143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507cf331789f9ed48c1ffc2a3f694c7d951a21084a84290c9884409cd74003ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_VERSION=2.9.7
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 06 Apr 2024 00:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
USER haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
WORKDIR /var/lib/haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba3dc9911acc47c015b8d4b1fe8c925a95c70fbaecbf9d775688d98bf1f249c`  
		Last Modified: Mon, 08 Apr 2024 21:58:25 GMT  
		Size: 292.9 KB (292898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9248e96ac2b81fa4b06e5a6bd6410ca0593af7817248d4e981eddcce154342`  
		Last Modified: Mon, 08 Apr 2024 21:58:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0686b8cb114e9093dca5191fb1057aa81bcc4022254d03a4e9554eb3158deec`  
		Last Modified: Mon, 08 Apr 2024 21:58:25 GMT  
		Size: 8.6 MB (8602780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a875960eff6b475d7aea1747f42e7a802666641432bfbaf2b52a9916a0d0887f`  
		Last Modified: Mon, 08 Apr 2024 21:58:25 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:62c82afaa6b36b9cca00ed9106f0ddff5a3aa4f2bbf0b26783aed2cae288c997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 KB (201227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d19ea577bca2f998201675d614ca1a569db1c82e0c1354d2e96d234c73753f`

```dockerfile
```

-	Layers:
	-	`sha256:7633155ec879018fa5460eb0850e653a008a71c604f084a183c1e8c9b51ecc6a`  
		Last Modified: Mon, 08 Apr 2024 21:58:25 GMT  
		Size: 180.9 KB (180884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aaf83c7e45d86776e298e3346cc3917d45c8ff18eab8f929659b7d3d5ee8474`  
		Last Modified: Mon, 08 Apr 2024 21:58:25 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:8781b16bd0828dabecdc6fd37bdfd0a8d1444de5bd96c251eaf217e9a3a9a68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12088994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0c908ad2e188129f00a4ef4c0666246e8c015e160902db5bfe50b95636d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_VERSION=2.9.7
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 06 Apr 2024 00:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
USER haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
WORKDIR /var/lib/haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9fed7e0409de566e5aa363e60666b69421abf2ca9538e8461489eabc61a2fa`  
		Last Modified: Mon, 08 Apr 2024 22:26:21 GMT  
		Size: 294.3 KB (294332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af16084ba21ae62fed4fab4830fe37d6693d5f4d0195b3d691afb74e383bc05`  
		Last Modified: Mon, 08 Apr 2024 22:26:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3feee9e8f61e82effc85c0e7e5fc58d56de2f4b93f11b1d1fc5ab94eddbe586`  
		Last Modified: Mon, 08 Apr 2024 22:27:14 GMT  
		Size: 8.6 MB (8627527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7bdd4754c80c23c08bad968af6861d57a285c973330f74a74414801aa70423`  
		Last Modified: Mon, 08 Apr 2024 22:27:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:54bb493ac1d72a93575e3f21e613ad3c2f220582e3cc5d4ac932ed0c19a6cc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899cc9d8b01e181a0ca404eac7ed5e58f52da1c6e911e1093c50d67747f4df0e`

```dockerfile
```

-	Layers:
	-	`sha256:1ef7cb9da50f8003b3ae343e24ef2c4829de2890706318789b816c5d13af3ff0`  
		Last Modified: Mon, 08 Apr 2024 22:27:13 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:a8191e896e29bcf7f1fc08902598ade96abe80359ab0180c090a7882675703f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11697888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b071a48a51298ef38344a5f97ab7266177e28a060c0907c145dd62548865df63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_VERSION=2.9.7
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 06 Apr 2024 00:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
USER haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
WORKDIR /var/lib/haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1689e7d0376c494e8d1687310b54ffcc64530b51182095eb858d61071b96f8d5`  
		Last Modified: Sat, 16 Mar 2024 15:44:10 GMT  
		Size: 284.1 KB (284131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a26fab690ff621278548eb7b911c7fcca4bc9f1989395798887eb560aac9bc`  
		Last Modified: Sat, 16 Mar 2024 15:44:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede51902f5763fcd907812362e04ad66d3318a43104edcfebd978021b6581eee`  
		Last Modified: Tue, 09 Apr 2024 06:35:55 GMT  
		Size: 8.5 MB (8493123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f733345d8808670e5b0e3283fd8e2d2fd8a67a4da8019278a6d0445b10c7802`  
		Last Modified: Tue, 09 Apr 2024 06:35:53 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b63a9ae300725c8b028f3833434209c7b2b3ef2cb187bbde829df8cb3f3b4d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf721b5bfcade7e4b752e332022bc1553f7b970c2f2c5e775ba492e98fac8000`

```dockerfile
```

-	Layers:
	-	`sha256:84a45388334eb238f0f5d3000176ffbc2870df29625b6f8f8359528b7f93cd48`  
		Last Modified: Tue, 09 Apr 2024 06:35:53 GMT  
		Size: 176.0 KB (175967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135acf93319a4c34ee04f2d66df0cb16d993ac63688742364ce625eff4b2bfb7`  
		Last Modified: Tue, 09 Apr 2024 06:35:53 GMT  
		Size: 20.3 KB (20288 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d4f0e353a91ca5cb1e1245830fc76beefeaa51d13e59371a52e10854d5126c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12249741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d2d3a02648ba8dd8740ef34e7c8dcc60c8c3f241c80745dcf996236bed33e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_VERSION=2.9.7
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 06 Apr 2024 00:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
USER haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
WORKDIR /var/lib/haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcda3649cda59cae8d81561479de563dca024e2b9f06ca6b00bf12932fd6f3`  
		Last Modified: Sat, 16 Mar 2024 13:23:14 GMT  
		Size: 286.4 KB (286392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591f6053915d2f2311d3dfda2c51236688bcb01ce5e07c66c118045360d06095`  
		Last Modified: Sat, 16 Mar 2024 13:23:14 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09f2d84998a53683090b244dac55723ec14bb23d90438734c301e8745f48080`  
		Last Modified: Tue, 09 Apr 2024 06:08:03 GMT  
		Size: 8.6 MB (8613898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f65dd37719362e844b19577f79c1ea5d4b1ef05a8195a08c7a8da446bcc6d29`  
		Last Modified: Tue, 09 Apr 2024 06:08:03 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:2745eb60a67acd760101802f6f5512c1119fb1a02b42dd9b10e9555dfbcb520a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4234b9627a66d0dbd3c93eaad9b83dd1f368aaed8de8c52f18b1ff34334609`

```dockerfile
```

-	Layers:
	-	`sha256:4e2b0c1f71dbf041595fc5538b8af39dfd2fa40ad9941078ee472aea15a169b8`  
		Last Modified: Tue, 09 Apr 2024 06:08:03 GMT  
		Size: 175.9 KB (175930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd570940a71bd5dcac56b90723523ba9b00a7175f4deadf69c002aa5660bf80`  
		Last Modified: Tue, 09 Apr 2024 06:08:03 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:c45490d82c7e2fb15384d87fa0f269bb34e923cd20bbb1ace094f79487769f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11941178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4963a97d6740e0a7e5cdaadb7e2986feea500ff0cbea813797100d539e5b6dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_VERSION=2.9.7
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 06 Apr 2024 00:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
USER haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
WORKDIR /var/lib/haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465914298fbd6ac5106c4d46fe0256ac1adb9dd15900e481b8487c51e0955d1c`  
		Last Modified: Mon, 08 Apr 2024 21:58:31 GMT  
		Size: 293.6 KB (293569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed6cd0320c25ba0b9a1ab02fdc889d0a8d4401dfb1a78f92bcc8c7cea537fed`  
		Last Modified: Mon, 08 Apr 2024 21:58:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc47db00db2cd0e4b8aac732fe04fccbf9227f68a9f047d018a74df4a25225`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 8.4 MB (8401784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1091a79a20559dfaf44d7557c5987e24cd8e620ec59142bcf7e5e061fb2ef4ef`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:26c7fe8152513f123f4ccfbddb49a9dffb87d064cc52a903eb71ef224aac2ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c60b7e5edd24a7a9046c5fe13e35440a6151432ad207910974dc9d00235cd0c`

```dockerfile
```

-	Layers:
	-	`sha256:919d534d746b293d943cb66024431158e71da5ff05d0370d7eba6f8478a6e749`  
		Last Modified: Mon, 08 Apr 2024 21:58:31 GMT  
		Size: 180.8 KB (180849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b787cc9d375e9d45cfbf195d3da7abb6189658fa8d5479765024a242f989281`  
		Last Modified: Mon, 08 Apr 2024 21:58:31 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e7caf6ead6abb86178752bf3c2938c538d0c969d25f7792fd5e6e84afebd44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12752104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfa6f51e9c36937341b69dc7a54d934e9fa0d9afc1be9eb82cc0da3301fd0a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_VERSION=2.9.7
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Sat, 06 Apr 2024 00:53:00 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Sat, 06 Apr 2024 00:53:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 06 Apr 2024 00:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Apr 2024 00:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Apr 2024 00:53:00 GMT
USER haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
WORKDIR /var/lib/haproxy
# Sat, 06 Apr 2024 00:53:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f4fc02a20d522d7e6f64be9775f2dd6f0afea62be74e048964ec50733e4e3e`  
		Last Modified: Sat, 16 Mar 2024 10:19:23 GMT  
		Size: 286.8 KB (286752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a064c54f3f3f27cbf3e7523a0e7949ddf0548e8ea20b4608bbca549f189e560`  
		Last Modified: Sat, 16 Mar 2024 10:19:22 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2cc47ade27a831aefbda2ff16b3ea9c324d7379de4ebf7af759bd5374e5663`  
		Last Modified: Tue, 09 Apr 2024 04:28:18 GMT  
		Size: 9.1 MB (9105262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179ef00c992915dea843cfac688a5f220043e1d2f9a715777e5852493634b1c`  
		Last Modified: Tue, 09 Apr 2024 04:28:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:58b276120f509085cd008b3ca02cd9285b3436a89db663cdce2d88792174c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16adcc856b5ce853ed5b7d2ac4942c18d5ff4e47de65ee6d1b54438dac206569`

```dockerfile
```

-	Layers:
	-	`sha256:dc6ddeb5e4c24d78a66a4521ff9ea207fc364ef3e6c5a10541e2756b12216028`  
		Last Modified: Tue, 09 Apr 2024 04:28:17 GMT  
		Size: 174.0 KB (174007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff5f70cba49cd6fc265dc984b04728855dbd4ac60861b037e346d219ce36674`  
		Last Modified: Tue, 09 Apr 2024 04:28:17 GMT  
		Size: 20.2 KB (20230 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:9a15447546e5104e536a3f1ff6ac60f1f4d87507e8e03e30b5c0f4343678d6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12331189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9082b770a393e86b8806a7f830e0a1213d83f2d4ab0ee6f12e1f45142f59a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8477608d4f77be9809c78a8c7a8765974384db87a94c5cc6091a7067f2159529`  
		Last Modified: Sun, 17 Mar 2024 20:18:26 GMT  
		Size: 285.1 KB (285096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060fc01df27265e71dd23a8b3395d1721b072c82ec68c8163682cbf5bd7919d8`  
		Last Modified: Sun, 17 Mar 2024 20:18:26 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbda1e20d1a1cb7f1476f7e6f43e0db62c03c8c2e1623f98a1d836384ff89f79`  
		Last Modified: Sun, 17 Mar 2024 20:22:19 GMT  
		Size: 8.8 MB (8801724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c04308db213d49e41ed3ea4fed094332b05a79c2bca14480855e710eccd98a`  
		Last Modified: Sun, 17 Mar 2024 20:22:19 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:0012da12de265a4854ee145ad43002bc1a40d4a3b7996f1a7e4d41399414abe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23309e3a34b4da25ce1178fdab6170ecd10b5eaaf31e7a0b13c99d531b9f72b`

```dockerfile
```

-	Layers:
	-	`sha256:017fd3f6dde063bdd9bee58183135b3e1c1aa301d72c245b77b56ea1a0efd622`  
		Last Modified: Sun, 17 Mar 2024 20:22:19 GMT  
		Size: 174.0 KB (173961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6e6071d6418fffd50037751894e2bc67387e3ef983f84b148086d42d3c7ae5`  
		Last Modified: Sun, 17 Mar 2024 20:22:19 GMT  
		Size: 20.2 KB (20177 bytes)  
		MIME: application/vnd.in-toto+json
