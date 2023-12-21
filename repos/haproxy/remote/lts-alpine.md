## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:d6159c7230193dcbcc1059ee7d9693b563ccd116bcfdb0418233bd9d56066a39
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

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:70a0e690e2317eddf92f9ef9f75df47f69c49d804e4ad1daf37024ba27ea3f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11926954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a44070fa3fe2971ad55c52ec1a18d8398d93f00e4fa4e7f95d4e62c8e1cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2c976f35a8ea75de33b1355b3b673c13e8f1658059ac174c5561f1cef79bed`  
		Last Modified: Thu, 21 Dec 2023 20:54:10 GMT  
		Size: 284.2 KB (284233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f426d7d43b54c7741ee554146f9c87f66a179dcb17d5803e332d2102e2b510`  
		Last Modified: Thu, 21 Dec 2023 20:54:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad03f98fdee3339ee317833d02000c4b6c12f87683f563d5bb0785b9b85704e`  
		Last Modified: Thu, 21 Dec 2023 20:54:10 GMT  
		Size: 8.2 MB (8232507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7ab39f81b0fab4f117de820e721906b50925a6770b2377d3ad0e3d6a2175f2`  
		Last Modified: Thu, 21 Dec 2023 20:54:10 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:02419f12d30e07732b0c0c8c0bfea5b15ae776818da197daccaef436ef6cd9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25ca90226b5ee0ae9ee85c24e89c1456be9fa2223afaf9447ce87d807c9549c`

```dockerfile
```

-	Layers:
	-	`sha256:d7c0b55ea84367a052efb480965800b6c7d53ccb7db9374d3ecf6b49330e36da`  
		Last Modified: Thu, 21 Dec 2023 20:54:10 GMT  
		Size: 151.8 KB (151757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff9f809961524572d60051e40245a66acd42ed6445ec33e0e816dcda00bed6c`  
		Last Modified: Thu, 21 Dec 2023 20:54:10 GMT  
		Size: 20.4 KB (20359 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:073d2f5ba4193df8eacdeabb9f623ff7234e8259b6ba9657328c20faefc32e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11531028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d6ceb1066d763c308c1896182c8a1f354cb806c225d7fcf7ab48e4e4e70559`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecdc091a79e672cc2c0d1a1068b2b25d27ca4a98f8c44df3552474d61c57592`  
		Last Modified: Thu, 21 Dec 2023 21:06:49 GMT  
		Size: 285.0 KB (284969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b3c585e3b6cdef8f32108cf36c8f6b4f4b012c0a50d15d87013840e52a994`  
		Last Modified: Thu, 21 Dec 2023 21:06:48 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a4e9f6cf65db3c6f5824f1309dfc0aca621b7e0a633611db74cabe1f85118`  
		Last Modified: Thu, 21 Dec 2023 21:08:22 GMT  
		Size: 8.1 MB (8079182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409e57c5010483e5e4db81400e458d100f28ba739917b82c3625536164b24118`  
		Last Modified: Thu, 21 Dec 2023 21:08:21 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:eee75dfdc37d25485ffaeb9525b3d923b2c234bb38784ef60d7ac83f1311d24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191316af2042a02cc4007554d97c23b6229baf90c69d7692699f5c3a1e942b60`

```dockerfile
```

-	Layers:
	-	`sha256:427701255711ee150dfd3ca1fb5ad2e4a60ee3aece275fbf78296e016d19ad80`  
		Last Modified: Thu, 21 Dec 2023 21:08:21 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:e4beb5a708961c3dffd022065330ce13dab038ca4807dab243247ae3e4e2e990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11161881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71136d2936b614d8093a8ddd9859ab80c496d040b59e487e215ab42d505bf539`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d3d8746c2c74e5291263a3c73d258d8d04dc50d43254f98ede324e51249c3c`  
		Last Modified: Thu, 21 Dec 2023 21:16:54 GMT  
		Size: 284.1 KB (284125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8099b3dc5ea43aedd718e4730fe45011daa1058581cb300585c1401c778afb`  
		Last Modified: Thu, 21 Dec 2023 21:16:54 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722edc5aaa8b3c8387b2b1bb90dcda5befba43f506f83ff96680b199778069f0`  
		Last Modified: Thu, 21 Dec 2023 21:20:14 GMT  
		Size: 8.0 MB (7957320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4721c1a0804b3b4d64165c3f5814d074a8cd12c25b20d3e9198e3bd8cf1bff5e`  
		Last Modified: Thu, 21 Dec 2023 21:20:13 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ce09998ce9ebd94e824b8afc9f0a9bcdc48aa6d379cfce56b409f06aeec8428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8074d7774bfd223693bbfd27eae2434716511c7659f159bb2b2989f0d5a0f134`

```dockerfile
```

-	Layers:
	-	`sha256:0b3413656cb1b38cee8370b2ae69044850da66dc9f5520a78d3ca9cee79b45fb`  
		Last Modified: Thu, 21 Dec 2023 21:20:13 GMT  
		Size: 151.8 KB (151809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ed0af95287d4a60e7ba3acc5e24bc61af3eaa33356b7128a6986900840b4d5`  
		Last Modified: Thu, 21 Dec 2023 21:20:13 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f35ec83d2f4e91d03c22bdec1bf2a8519b45c445c3af27f475c0b6112a97526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11822654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29e22e87b58992bf7f6a0e1a6247477a827ce91a5e0a4fe60e51dbc06ba35f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fbd9aa83fdb62960cd6bc5d57aee7e24030f2c19efdbd2b510a73da6d55e4f`  
		Last Modified: Thu, 21 Dec 2023 21:18:31 GMT  
		Size: 286.4 KB (286390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3156417240324d1a1e14d4da649ed8ff9e13897121684396f4a631cfc8d7a4`  
		Last Modified: Thu, 21 Dec 2023 21:18:31 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521103b035c280ad95b7d37d4f9bad43bc7c2064623b6100014496531ee1c015`  
		Last Modified: Thu, 21 Dec 2023 21:21:40 GMT  
		Size: 8.2 MB (8186735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158143c2a8ddc0c35f9dc2763ddb1e77a9f3a8d4f68a31483c65c3d392f9974c`  
		Last Modified: Thu, 21 Dec 2023 21:21:39 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:c48d7a21c1012c4a3190ddfdc262949586715f1744ae598e6da4242d225a3d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 KB (171978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed7bd013508333f200cbbd4093ffa9a37014b4ba2f7f469a4c3779d3691cb55`

```dockerfile
```

-	Layers:
	-	`sha256:b3aeb2de702ea5ef483707b221e6d2f3707330f144c99b9e61e17ebbe7cb58ee`  
		Last Modified: Thu, 21 Dec 2023 21:21:39 GMT  
		Size: 151.8 KB (151772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62c382d8c5475f6ccf1ac367b366452af8204a65837f646230100579ed5c9b6`  
		Last Modified: Thu, 21 Dec 2023 21:21:39 GMT  
		Size: 20.2 KB (20206 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:495f00a44c8c3845c65689f92d1b2a9c3068fff87b17f5e437703fc012b0523e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11565607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1c4a285776fe05f268a29fb322438f52398afc673f81b50e397c4125bf26c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bd1cf6fdf25045d30c0a651fb6060f48711bd2442c919e22d911c71083cc5d`  
		Last Modified: Thu, 21 Dec 2023 20:54:16 GMT  
		Size: 284.6 KB (284558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0510b2d4c7546c277a3ebfc98e307a540f82aceca3f1893e71b88e9f67979a80`  
		Last Modified: Thu, 21 Dec 2023 20:54:15 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51d3595b950a2c46959d89c46417a8acf2587c7e4bd554368c5b40bcd0228a`  
		Last Modified: Thu, 21 Dec 2023 20:54:21 GMT  
		Size: 8.0 MB (8035200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42739204bb223ed3f0da754f79d3fc64141296b5cb04f327b3334d132215447e`  
		Last Modified: Thu, 21 Dec 2023 20:54:20 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:eece54c68bc370418d91fd1b95a916c040e130a5d8e201e3cd4b268b220db44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 KB (172038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0168c1282c0a01d2429a1eae3f133d5eb0355e4d1107f229ac358a31d490ccc8`

```dockerfile
```

-	Layers:
	-	`sha256:e78a1fa1c77bfa2b95a26e4581b0de4ba9956caa3e0d9000b4bb1f2338dfc742`  
		Last Modified: Thu, 21 Dec 2023 20:54:20 GMT  
		Size: 151.7 KB (151722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bceed3eb23198757859e6132b22c8bff1a7daa973e8dfed2b1019a833a9fe03`  
		Last Modified: Thu, 21 Dec 2023 20:54:20 GMT  
		Size: 20.3 KB (20316 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:d0d05ab0225bcf623b952b068835d470b21bf0b85ea09bf2db5510e222c7af03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12252022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad478a5b8827389ac59c4a582cc683ab585897a5b6a9bf375a8838d8b3a844b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98add8af217e8bc0654a56f2c3fb96087d6f2e9065f0e0140e9e67344d6e198f`  
		Last Modified: Thu, 21 Dec 2023 21:14:22 GMT  
		Size: 286.7 KB (286749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fce80216432664e5aa167af2783e26605301807281088bae4c16ec8614ce4d`  
		Last Modified: Thu, 21 Dec 2023 21:14:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b36784518b114a9bd8d855c0f3be80749ccba9a032c357e6311860b7203f43`  
		Last Modified: Thu, 21 Dec 2023 21:19:52 GMT  
		Size: 8.6 MB (8605303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39ec89d71ed9b06dffa398948be91ca17f99ede866c24937025e8c139cfe42`  
		Last Modified: Thu, 21 Dec 2023 21:19:51 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:1f07e8f35c2d2281159be39d007e52ea1a39d432507ce3729cdd288680ac374a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 KB (170414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b097e5079c46ada1388c60d855d6181a94cfa3545ee8918c3275b55431ac7c0`

```dockerfile
```

-	Layers:
	-	`sha256:1e01af84d35b89bd85327307e81caed274fcef87ea359c5aed22daeadb7dff35`  
		Last Modified: Thu, 21 Dec 2023 21:19:52 GMT  
		Size: 150.2 KB (150167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49ee054028e9c1c3a757a6f65282f9299b431f5b6c668fba8f96fa4d468e016`  
		Last Modified: Thu, 21 Dec 2023 21:19:51 GMT  
		Size: 20.2 KB (20247 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:977be384ead5fa8484c62adca12035be8210ad8af6ea754d0048116614b836d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11924221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7d513ee4628e72be1b659aba82432f18aed15a2d95ff28447109a10c997d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109edadf9cf9d61de46da008672376ee510e24bb92e48c96f87940826ad7f348`  
		Last Modified: Thu, 21 Dec 2023 21:06:24 GMT  
		Size: 285.1 KB (285084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7d9f59c43d7c3431b235d64de5c1bc635ee4c102a6623c9be89f4f9eba654`  
		Last Modified: Thu, 21 Dec 2023 21:06:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c929849c331036a41e22895b3f732affd40b5757c396995423539af234a00b`  
		Last Modified: Thu, 21 Dec 2023 21:10:36 GMT  
		Size: 8.4 MB (8395067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d38c118eba17ca3eb5e483dfbe78792d99641c604fe0df3deb28a225a0950`  
		Last Modified: Thu, 21 Dec 2023 21:10:36 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:60ba836e23336e96f8cfe2da5ec8194752fb35124f2f30b65a9e77c19259dc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 KB (170314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdde4c57bbd0c9ffc3a6f6140fea7500b137a263fa3c4484a7dd02ef83ea7a29`

```dockerfile
```

-	Layers:
	-	`sha256:e6d1195145e319b4f799a897be40a7628728418b6f2a1272bb6c8b32e433eee6`  
		Last Modified: Thu, 21 Dec 2023 21:10:36 GMT  
		Size: 150.1 KB (150121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57229e8116a22045ea4be0a504d1be8d0ce2200eeb46a72a11679b9a81450cbe`  
		Last Modified: Thu, 21 Dec 2023 21:10:36 GMT  
		Size: 20.2 KB (20193 bytes)  
		MIME: application/vnd.in-toto+json
