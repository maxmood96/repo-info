## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:c3248042dee976f8fe15bbdb37103348537a142ac9a899d937f0c989ed4c2c99
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
$ docker pull haproxy@sha256:1ab3736538a0640230f2bb49587f1df26afd5b547bc32932d2fd34fc63024784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13119727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8880a966f98fc8335a9c088f44dd66a1b72d6a007e2d45fcb26e0afbc41787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c954c1e06ec52bead7692c2afce1a6d52a0c5b532a97aa8c7952ee1dc1188949`  
		Last Modified: Mon, 22 Jul 2024 23:04:29 GMT  
		Size: 290.9 KB (290871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16259679e6b1e48cb53c2a87f54bafce5128bd5d5ff31427933114479c303b52`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836daaa71c785a6699581d10fcfef14bfa8fa13eb66ec6809ab658524959061b`  
		Last Modified: Mon, 22 Jul 2024 23:04:29 GMT  
		Size: 9.2 MB (9204516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ddb96577bf3bb048136041845e74be40d593973062674b6e44c918f8efea63`  
		Last Modified: Mon, 22 Jul 2024 23:04:29 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:504c8bbae7a0873c36bd061944a89119c1794009156f8c99d1500550ca475bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d9da3ec9b41066000d616f1ac3d5e562034c9bb3b2ef9fdbd537adef4959f`

```dockerfile
```

-	Layers:
	-	`sha256:745c7b347b156caef4f56113c40a5ebeba4d3ca158053ac8eb460b407d014d10`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 180.0 KB (180006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603f2b5d77c64de6bd44c62890977b06bf0a8be1e1af0858ca43f45e8685a9ad`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 20.9 KB (20850 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:b38ffea6415f516fbb5778873a0b220b0fdbeb42b6b5771d7f59f67547538362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12877253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a783669c80c0e21fada9041776ca1d35729c574a610013198cd477437508b82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640327ca2803cd8403ef22832532196cf4bc018bbac029c968c7144f3c77b24a`  
		Last Modified: Tue, 23 Jul 2024 02:56:19 GMT  
		Size: 291.8 KB (291772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac09fa4dfceeca62ed61bffde759456d6bb3464a25b3e0ef0d0fe8f220a05c92`  
		Last Modified: Tue, 23 Jul 2024 02:56:19 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c0a0ef111966349553585dba67cc90d15a59ad6681cf34daa8cada80b7870b`  
		Last Modified: Tue, 23 Jul 2024 02:57:25 GMT  
		Size: 9.2 MB (9218840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b6752e8bf131b38e4252624c6592abd06157a867186509412c806f07c0971`  
		Last Modified: Tue, 23 Jul 2024 02:57:25 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:fbdb7e2b69a9cae7e2b53592087e9983391827c8f83f5b64ae38661f93d6a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746c98cc1c6069a59fbace1d29db97755e511f95e648a6664a48c06d60aa30b9`

```dockerfile
```

-	Layers:
	-	`sha256:4ef17da59759c7e0da9a8cb4c4b09407e42308fc00d32d57fe6e16f3f6a5f29c`  
		Last Modified: Tue, 23 Jul 2024 02:57:25 GMT  
		Size: 20.8 KB (20759 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:aec057b633dd757dd3bc75ea1652ef09fbcc48d83473d898578ca401f5d9dcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12457157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1162466a3b51626aedb96824bfa355137965a2699742d568711a75953d0a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8c007486c4ebf928f3277bab02e9d19dcbfbc8bfdad34259645ee9ea6ce76`  
		Last Modified: Tue, 23 Jul 2024 17:36:48 GMT  
		Size: 291.0 KB (290951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279b9aaf87869a3b06cb493365b97cb6afd90eedf525204d8c768f2a66d0d747`  
		Last Modified: Tue, 23 Jul 2024 17:36:47 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e2bc792abf474f9e483e779cb42301dbeae2893e07e4ec620e7a22968174c`  
		Last Modified: Tue, 23 Jul 2024 17:39:07 GMT  
		Size: 9.1 MB (9069799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001795c858ba86017ae9f7f7015366b698688e2687494df0f6676e8c2365ec6c`  
		Last Modified: Tue, 23 Jul 2024 17:39:06 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:7493043ba695ae98b9aa5c88a9c8967a6d1f2e4b0d887e567d750e3795b7d5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a1c84074b66b79dd074f4131e0035be2978d634ded2d0910e12f0b8b5ecc66`

```dockerfile
```

-	Layers:
	-	`sha256:bfd4273568f0ba7a0eabb5493f5f5a5084138118e972851e5beba63cec041236`  
		Last Modified: Tue, 23 Jul 2024 17:39:06 GMT  
		Size: 180.1 KB (180074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d03a3fd85d1f1364ced414eec4c374084614cac2334d885258aa43e26d7f29`  
		Last Modified: Tue, 23 Jul 2024 17:39:06 GMT  
		Size: 21.0 KB (20977 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:8d389edd1464e49d42752fbbeefaecfca8c93ce1ab13c616f0708d044f7ea824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16418080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c07893a94b616b92c4eaf7d302482eccae5c12128abe0dc2a102b56aa0e7927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc324bb4ec00801c985d4c7e26a2066d8c6dbca296dbed880d420d7f444b0b4b`  
		Last Modified: Fri, 12 Jul 2024 00:58:32 GMT  
		Size: 293.6 KB (293585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e33d15baf37270282bd36fb3ee671d39f708bf4ae5f51b7debf43308425d550`  
		Last Modified: Fri, 12 Jul 2024 00:58:32 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06363e5af8578519488d3f752e722ba291b7d708da9c0417afca75f230e3839`  
		Last Modified: Fri, 12 Jul 2024 00:58:32 GMT  
		Size: 12.0 MB (12034250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec006aa9558678ea362ce6c12e146f382658f4e602b50f13d0f7e368179de4`  
		Last Modified: Fri, 12 Jul 2024 00:58:32 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:c03a20cc85ecf6ba8f2d2c66ad507d0061ad684e1402dc6edaaf4ddc45197f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 KB (198878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3995665f32255855a8c1c5099d624ac7facfa305f3c7fcdf7bcfe07636b85cd2`

```dockerfile
```

-	Layers:
	-	`sha256:0518095e18c050fdab429eb7bb8a490d51a6b2504b6cf38a088ccef7cafc567d`  
		Last Modified: Fri, 12 Jul 2024 00:58:32 GMT  
		Size: 177.7 KB (177677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877c417bc7b022db858acbd979468ee3ba549759bb4ff32fa6e159c862f8d5d8`  
		Last Modified: Fri, 12 Jul 2024 00:58:32 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:2e4af47ab048a30b6e4d0a8b9a52cff4630396d8a0761b785da967f2f7dbe101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12762707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6911fe8082163cb27c55f7eb00969bba9f83421b0f64449f2aaf4d2a6f1c5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87a639a878dc21ea47730425fb3f46ab01597d024637a28443fd78e5a711657`  
		Last Modified: Mon, 22 Jul 2024 22:10:29 GMT  
		Size: 291.4 KB (291365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09433ee5645f3159433c4b58512e84bfd6d302ecdff1642b8e15e71e549bb`  
		Last Modified: Mon, 22 Jul 2024 22:10:28 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06881169c32371c1230864b001eacc0fdce5358ceb0a1aa282ae52c64c3c9e78`  
		Last Modified: Mon, 22 Jul 2024 22:10:29 GMT  
		Size: 9.0 MB (9001819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a0dbe4f72140d54fdb0aede29f045bf30f9849d35f899f7079c736eaecde1`  
		Last Modified: Mon, 22 Jul 2024 22:10:28 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ea384d5fb33120d793fef2a5e695d194b4a7ade833070d2b567027cf36e69c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 KB (200758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a984998b27b8aa0e49132e549999016e47aafc3b0ddaa57a1186669c040ce9c2`

```dockerfile
```

-	Layers:
	-	`sha256:737bdc686e8ec21317b574ffd91dba402ed852ce21b6b55b2c1d304481290700`  
		Last Modified: Mon, 22 Jul 2024 22:10:29 GMT  
		Size: 180.0 KB (179961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5e113f1eee23c2e65471b40e360e5f1081e19a95fbffa2622d7a337fceaf46`  
		Last Modified: Mon, 22 Jul 2024 22:10:29 GMT  
		Size: 20.8 KB (20797 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e629e5880b0d7c665a97a10f67225ca5843ed28d404d2903647926f03441c844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13603172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757ecc4551e1251e80dc341cf02b23fbc46b41a3d4ee056c4ec6194e42a2bc39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149fcc152ce35c0a49607948c7e71614ffda2e49d429065b8fcd50d103f43936`  
		Last Modified: Tue, 23 Jul 2024 16:57:43 GMT  
		Size: 294.0 KB (294021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4f61261509eceff2b033827203b9898c1a8791baedfba483ea2c009a5aa88f`  
		Last Modified: Tue, 23 Jul 2024 16:57:43 GMT  
		Size: 977.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b9945dc17c7702bb11dc4225a20791593e2962e07dcce7d1c67976a58ac13f`  
		Last Modified: Tue, 23 Jul 2024 17:00:04 GMT  
		Size: 9.7 MB (9736146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6291b30fd7b6eec01d3b10d5535b8556732c9743e986163182cc1cd02b0c8f`  
		Last Modified: Tue, 23 Jul 2024 17:00:04 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:49a49776a6cc341657e012f1974a51ac6cd279c973860a5d7ab01b9c8f5a05cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (199026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373c355334460f15ccac0a770d0026f5d1cbbf5345a476650ae7d053266734af`

```dockerfile
```

-	Layers:
	-	`sha256:8c69b3be283805d992cd8dd0864e697f26a0e7434b7b564ce5a44d7ef38339f9`  
		Last Modified: Tue, 23 Jul 2024 17:00:04 GMT  
		Size: 178.1 KB (178110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73290f2e9527d5c5e491e87f7fa30413acfd0ab3717560fb828678c400fb4c34`  
		Last Modified: Tue, 23 Jul 2024 17:00:04 GMT  
		Size: 20.9 KB (20916 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:ab59f21a5fc5e868720de32f29ab866b1577541e85d6f3a89aa0dbe8cd2a595c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14646995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985a14a93834ba8850b8c6d67a71cc152886faa04e3a52ee641d6d05190f7f5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c24825b8b31b8a815c59c4006fbd84eb8c5e80a705a9f84ee453c5d0dcad0a`  
		Last Modified: Fri, 12 Jul 2024 01:05:04 GMT  
		Size: 291.7 KB (291712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b708b91087f36370890d553377e61798cee1871f5d7e4f8627f59090e19901a2`  
		Last Modified: Fri, 12 Jul 2024 01:05:04 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30366268700ccdf64894411f0039952be5b34f47183d3ca3c3a4dcbed3fc5677`  
		Last Modified: Fri, 12 Jul 2024 01:05:06 GMT  
		Size: 11.0 MB (10982789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c0fadc38b4433824c7b6516c1f98f74689f9a0e6e8d5367369adb605b468`  
		Last Modified: Fri, 12 Jul 2024 01:05:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:2d70afbf95a240be2254e5da6c3c02f6cb348f95fcb82cfc721afad9ebf8d295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 KB (196591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2d46a1c946fd8affeb9f4da45fa3ba52c14e1b80b7f8177778815b64f6003`

```dockerfile
```

-	Layers:
	-	`sha256:1e2c954b850082352d109df641b9535904de0bb5315955efafdefa5b56865f31`  
		Last Modified: Fri, 12 Jul 2024 01:05:04 GMT  
		Size: 175.7 KB (175673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acbad7539fb063dde8b69b1da3701d3329de41c356bdf5c7128beffa5aa5b6f`  
		Last Modified: Fri, 12 Jul 2024 01:05:04 GMT  
		Size: 20.9 KB (20918 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:cfa7b20e8d03672c15995ade82487c1228e5a3520ead854a625921c750dcb9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13199625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ebd796a8a6ea85e2526b01b0b626f801ed6ec44c446edca3e3c50c9c92987f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bd4f74527e7672eea9254b95edbf1ed4bdd2c9b6e150f7e891302cd11cb0c`  
		Last Modified: Tue, 23 Jul 2024 16:14:48 GMT  
		Size: 291.9 KB (291892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d74f8305aa7b2c9df7a2b36b63e10cd6370598cfe141dc11fed5bae4ee2b493`  
		Last Modified: Tue, 23 Jul 2024 16:14:47 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262ce9b86c8e4bfb0e29699dc70b13c53a887ee9f946486921f245243487b5f1`  
		Last Modified: Tue, 23 Jul 2024 16:17:11 GMT  
		Size: 9.4 MB (9445215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa69a1b04e06b04d91661c6e594190767038feded28eb2a04c2143d3fa81cfc`  
		Last Modified: Tue, 23 Jul 2024 16:17:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ebe0989359261c09ce31e8029fc3a10609681d35975042a2789e154fc46a03d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 KB (198901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ee49280629ce50535ceac5dd55156533d21e40e2c7bef9b62fdcc1869050f3`

```dockerfile
```

-	Layers:
	-	`sha256:ff0e2ee17fe4ce46728b3da27525c7dcd938978a63f079a8911f8a40afac4d3f`  
		Last Modified: Tue, 23 Jul 2024 16:17:11 GMT  
		Size: 178.1 KB (178052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12ae447cc2919b8c23320c784609ed88378913956d6a8cd21159a40d596e684`  
		Last Modified: Tue, 23 Jul 2024 16:17:12 GMT  
		Size: 20.8 KB (20849 bytes)  
		MIME: application/vnd.in-toto+json
