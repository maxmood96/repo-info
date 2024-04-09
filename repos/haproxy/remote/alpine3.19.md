## `haproxy:alpine3.19`

```console
$ docker pull haproxy@sha256:eeec38902f8d28a7de2e9408105c246b9fad2aa47252a22a6d5aad8404f48e20
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

### `haproxy:alpine3.19` - linux; amd64

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

### `haproxy:alpine3.19` - unknown; unknown

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

### `haproxy:alpine3.19` - linux; arm variant v6

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

### `haproxy:alpine3.19` - unknown; unknown

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

### `haproxy:alpine3.19` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:420e72b2fc3c89822dd7b1e424cbe346ce00320399d7b820ab9b081743f0357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11652133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449943f5835ed2d93148465bd0c7c00f0229238f155ae0c5bc0921d073e0d58d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
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
	-	`sha256:00812e699863c485a43026d4e1f2f90508a4e7d0f7a3c0e563c0ef36ca6e658e`  
		Last Modified: Sat, 16 Mar 2024 15:52:48 GMT  
		Size: 8.4 MB (8447368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27ecd6cd11479a2e3b3e27a87bb6ce35befbf096b3fa6f1f5674b986083bba8`  
		Last Modified: Sat, 16 Mar 2024 15:52:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:eac517f0c39459a09c201ba7041ce6c4ecdcf8bdba5f7acf5dfdb3bd731468fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941f6d814a1a652e1b63393bbdb875218ff374da9cd170d6c9d7b391a7a1c9ca`

```dockerfile
```

-	Layers:
	-	`sha256:1a9e4d0edb286122d6d28e38fcb47725b68c9ea48722884b209acbf7d78efab8`  
		Last Modified: Sat, 16 Mar 2024 15:52:48 GMT  
		Size: 176.0 KB (175967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89eb6b3d36675af1d8d4acc8691b6e27972161229fa359cf9847b3f45fbf950`  
		Last Modified: Sat, 16 Mar 2024 15:52:47 GMT  
		Size: 20.3 KB (20289 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2d510db5a4e1b34bb9978f208094cf71e93ba76e450c9f83db44a016cecae6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12214697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6930329d1bbbd344c8ccf7e4e80d1efdf0e2466f33caff01342b7c10e70d993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
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
	-	`sha256:9ac45c466d0a65437084e6afde3ba6acdb38e76ffe97bd9bf631532d06c988d7`  
		Last Modified: Sat, 16 Mar 2024 14:09:42 GMT  
		Size: 8.6 MB (8578857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547875d895e94c53ec9fb077931874a117cee7a9ee8c0e94e49a88a5e0eca56f`  
		Last Modified: Sat, 16 Mar 2024 14:09:41 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:a61becc4367c6e3a13abf4a8a7e91fb35c5965d2a7a3491d6214f93a2d5c7dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16adf5f3ce8a89aaf21279a5936faac509913cda0e56ef04ee2843c200cefd4`

```dockerfile
```

-	Layers:
	-	`sha256:d57f7b56152feb016a89b9a2e8a6f1c1467993fff61e9cd50dcc2a11c28db458`  
		Last Modified: Sat, 16 Mar 2024 14:09:41 GMT  
		Size: 175.9 KB (175930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30e50ceb991df1eb43395dbc9f35575b1b66cb528dece092d8c89a90af51d131`  
		Last Modified: Sat, 16 Mar 2024 14:09:41 GMT  
		Size: 20.2 KB (20190 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; 386

```console
$ docker pull haproxy@sha256:b13b07b5da724bc6600120f1da383669a4f94839de1e04927bc82acdf6c3c33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11897110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669ac168c2dea08d6301c3df9184f1bd32e9d69a8e688b70098e2631f31bedce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c793b8a7069eac52ef57b309809a0c4e85ca41c1eebbe66a8924c692e6f2829`  
		Last Modified: Fri, 15 Mar 2024 23:54:47 GMT  
		Size: 284.6 KB (284564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd55503e728c22114684c8c90ceb10c8dba22befa8b4c0a391447c45b665370d`  
		Last Modified: Fri, 15 Mar 2024 23:54:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2ba3103fc490ba6014440aa6afe93b566372bff27eb1cf7b30e3fd5a7cde57`  
		Last Modified: Fri, 15 Mar 2024 23:54:51 GMT  
		Size: 8.4 MB (8366724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368308c71703c698ccae3b9eaef5d3f260daae1754ff3fa2bbb9fb69f91880a2`  
		Last Modified: Fri, 15 Mar 2024 23:54:50 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:2ae7c6e59976293d4fb468b20d2a78e2b84d1ca2b8165cf381a4f070c4b4f5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 KB (196180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fbe857c2fec80764cd07b287342a94e33d5396fdb88c718e72841b83b8a1fd`

```dockerfile
```

-	Layers:
	-	`sha256:d0c27fc80774122bf8e1f7a46e0739138560baac6880584a22af7b148eb4c7dd`  
		Last Modified: Fri, 15 Mar 2024 23:54:50 GMT  
		Size: 175.9 KB (175880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bd62f91e88086d9e273c157235d4276f576d26658a4f2757f7fbb24e441dd7`  
		Last Modified: Fri, 15 Mar 2024 23:54:50 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e9651cbb0c8ef2b4f2d04c7b575f41f890a61ddb891d0737cb1878dad709922c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12712779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90452bd6f0066f2f8a88e7002509fde5b442f19b74b4a3a2ccc4138fd816f235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
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
	-	`sha256:46d284a05e79a960b1ffdfa5c4c6c6ce21ff63f7dcec1ea9fea971aaa2b79726`  
		Last Modified: Sat, 16 Mar 2024 10:20:09 GMT  
		Size: 9.1 MB (9065937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe13f5524a37408b516a160d97f5e7d340ff262798bb1d4dac5c038839446ef`  
		Last Modified: Sat, 16 Mar 2024 10:20:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:1e7efdef6f4a597d1c5bf45b1c8f9bd2874fe5721d4e579a226e08af0a0e0077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760da8845576f7ddf2aa520c82062cb63d4a91ed5921375e57ee0137f8e5ba88`

```dockerfile
```

-	Layers:
	-	`sha256:b8073ca4bc2e8b9e64881295c36884544910066e4c3599e69a24fc2a67b64a58`  
		Last Modified: Sat, 16 Mar 2024 10:20:09 GMT  
		Size: 174.0 KB (174007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d9a1b18995744aeee65e35f8ec4f7d30f5cc2461b7e9525d60ed04b73cdf60`  
		Last Modified: Sat, 16 Mar 2024 10:20:09 GMT  
		Size: 20.2 KB (20231 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; s390x

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

### `haproxy:alpine3.19` - unknown; unknown

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
