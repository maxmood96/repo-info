## `haproxy:alpine3.19`

```console
$ docker pull haproxy@sha256:adafd090bc4b7f2a4867069f3ebd3f886e3820a95b305049d87f02cfdbd8057e
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
$ docker pull haproxy@sha256:97e303161ef433581797258e0ccc6b64c43286bf93a6c353c7e5be710a9109de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12261193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f19e81fd7edbd7f31fd9171e1a28e833e0675aa6351c117a430de4d3a5e4573`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_VERSION=2.9.5
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.5.tar.gz
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_SHA256=32b785b128838f4218b8d54690c86c48794d03f817cbb627fb48769f79efd59b
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 16 Feb 2024 00:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
USER haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21381923d333ac00802220cab0547fd10c67e3974e1ada92f739a90109027094`  
		Last Modified: Fri, 16 Feb 2024 19:51:49 GMT  
		Size: 284.1 KB (284103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c68a64edb5e88f8201a258b7007dc107b271b5da384c052317b7cc3c3aae798`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33746a6f114fea19ee770830806d070db08928f48e33c7b7b0ad454412aa2a7a`  
		Last Modified: Fri, 16 Feb 2024 19:51:51 GMT  
		Size: 8.6 MB (8566625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a71516a09cfc1f2f5f3e8d14b35027c3bebe48c2bcd783be39173fb05d9c3`  
		Last Modified: Fri, 16 Feb 2024 19:51:49 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:75cea40b9a97b72851663a5d25bf066cadd5b4caf73617487b3b206f64b29f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd628e77f44b87f8dae5d13473da50fca8d187f7e801012206bfc3ee4c2e11c9`

```dockerfile
```

-	Layers:
	-	`sha256:6c48ed5cd7460f8680d7e9dd727333cf2424ae9cc942c48fe06f4134138e47b0`  
		Last Modified: Fri, 16 Feb 2024 19:51:49 GMT  
		Size: 175.9 KB (175915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de882b34125c8f8bdee07d71f17bfb8d772c22802c08092656b516575e98bc8c`  
		Last Modified: Fri, 16 Feb 2024 19:51:49 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:cd35041a4d5585f9400a2b605e231cc7984096615f57d7efc20c90f721bd6f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12037609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1c4912f6100b45a11b9c7e551be7d72afb36d1b8a593a2712f3079f5a0689a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_VERSION=2.9.5
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.5.tar.gz
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_SHA256=32b785b128838f4218b8d54690c86c48794d03f817cbb627fb48769f79efd59b
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 16 Feb 2024 00:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
USER haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85b233432e251d0de4abe1b2c20dfe2d45ec02e9a7a8538ee8eebe26145977`  
		Last Modified: Mon, 12 Feb 2024 22:13:36 GMT  
		Size: 285.0 KB (284969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975d9dcc5ea16ab012a0d6d906197cad7511267e73bba790ac96568a5b4f948`  
		Last Modified: Mon, 12 Feb 2024 22:13:35 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f358fcd94632a90bffc9831a57c7e42e60ead6a76605bd04d858e12250647e9d`  
		Last Modified: Sat, 17 Feb 2024 04:21:51 GMT  
		Size: 8.6 MB (8585506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add895e922f06d66d5376dd8895694a7a6ce7ccaee1ece557b1d9b94428690c8`  
		Last Modified: Sat, 17 Feb 2024 04:21:49 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:477c6fb899134a5f9616c2aabc5c1a407759c69b2f3d0d17955ddcf1c169d3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144dd112a31e3ca0b48426e60c1e3dad65808a94cf46499a8dd2a6a9bd403362`

```dockerfile
```

-	Layers:
	-	`sha256:abb9b189f462102efdea4a863a43313e47a626177fe1cd3ccc318e79a487d84c`  
		Last Modified: Sat, 17 Feb 2024 04:21:49 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:909aed47f4ed1f640619ecec0727a9b6bd1aae09582e0cd22a2f7fb2104abaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11544982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f0934f6ae8aabad306adc2f3a537458f769cd8417e9c560e1ec0e32ca9bb33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34457f305359ab30eac9a9890df125c672c840e6448eec07d80321c3bac0a29`  
		Last Modified: Sat, 03 Feb 2024 09:41:43 GMT  
		Size: 284.1 KB (284127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f278677e1da6524e7094dc917e821adc1a7434e6a442d28872bbf23b4304f`  
		Last Modified: Sat, 03 Feb 2024 09:41:42 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977e86532d96f279846815a84b23f4af4a26b4d01ad68c7fc48387b625d89d24`  
		Last Modified: Sat, 03 Feb 2024 10:20:18 GMT  
		Size: 8.3 MB (8340225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc44be97653dfc04ff70e8bc4c88258a6b8330dd05667657f168c1a3a196bc57`  
		Last Modified: Sat, 03 Feb 2024 10:20:18 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:38cc2467c68a9743f4877a51792ac5e14833809a4c150fb7101b8e909e663e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f1d0e01d039235b81bd98f35e7f595220653fcea71f312eb1e7ab59922126c`

```dockerfile
```

-	Layers:
	-	`sha256:1a5d4a4320b41d4e37a579837e5ea5f7ce2e6fe12652bd00fad2bb34c3d4a0d9`  
		Last Modified: Sat, 03 Feb 2024 10:20:18 GMT  
		Size: 151.8 KB (151799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6275f22bb3191f95296a7584eed1fd0844797e150c355e6cf283545791d1b1`  
		Last Modified: Sat, 03 Feb 2024 10:20:18 GMT  
		Size: 20.3 KB (20289 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:abd87fb7847b6ea14ee75cac5a600fe1e46c6b8a2abce6371cf30db21268d4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12213089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac155583a491abdde6a895991f2f64b31752440d82be23fc5b438b0d8ceb77ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_VERSION=2.9.5
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.5.tar.gz
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_SHA256=32b785b128838f4218b8d54690c86c48794d03f817cbb627fb48769f79efd59b
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 16 Feb 2024 00:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
USER haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffdba998a7d9cb80d56d3a75f4823cbc595ce14eb785a35376c8d2f7f48855d`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 286.4 KB (286386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d642c0f21728d496d6aa268bd2d344d9e3c63786f31cd6e353da1abea11b47ed`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b798e04c30c4cdd93fb80ac0e1142ff6f6ebe2e843e3a5c0b39adc5579084ef`  
		Last Modified: Fri, 16 Feb 2024 21:05:06 GMT  
		Size: 8.6 MB (8577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a8b4db3a8b89e288ff64b8015309a2af95ae04990c2f0a4155f010995ac70c`  
		Last Modified: Fri, 16 Feb 2024 21:05:06 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:7598c1f046f777b2b4fc67268d3792ed4ed467bbbaf9c7f5577df65846609388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9f4252340bd56207816e5c235b1e2d00c721c119fc12978e27d254da09cd57`

```dockerfile
```

-	Layers:
	-	`sha256:d3175f1e21ed27a944a4cb819d1fb574d25d1cc1b3a72afbbb59c7e7545d53a8`  
		Last Modified: Fri, 16 Feb 2024 21:05:06 GMT  
		Size: 175.9 KB (175930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89677b881693a5b6c65efde7485dd3479933ead848f168deafba90914b39cec`  
		Last Modified: Fri, 16 Feb 2024 21:05:06 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; 386

```console
$ docker pull haproxy@sha256:d3c3954083d764b411826ccbe79435f065ab20a2488d0ddb99adcfe633cba3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11896271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d159a69a1ca1fdceab1501a3bbb57e807d05d4914af9dd5d7d63713227abecf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_VERSION=2.9.5
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.5.tar.gz
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_SHA256=32b785b128838f4218b8d54690c86c48794d03f817cbb627fb48769f79efd59b
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 16 Feb 2024 00:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
USER haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca37edf6baeba40a712145fec483190b2549f8d3cf787efa091f148186413a5`  
		Last Modified: Fri, 16 Feb 2024 19:51:52 GMT  
		Size: 284.6 KB (284564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c6b294a0933b58e05eddcbef2a15a03750fd22832cd9494fc26d6b1031c776`  
		Last Modified: Fri, 16 Feb 2024 19:51:52 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f1527b67db07b3f03bdfd46e744bc34969b24dd31814241767c54f377a76df`  
		Last Modified: Fri, 16 Feb 2024 19:51:53 GMT  
		Size: 8.4 MB (8365884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421e5424c8326731825847e019539e338209fd7b3dc0e5079faa15c8f9802e5b`  
		Last Modified: Fri, 16 Feb 2024 19:51:53 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:9558a01d1abca58417267ae0575a590b87133ad5001a455cc3c98b0e37df5207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 KB (196179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d15b3466c1d22b38f0e430dfd28f5b2dda2a9e3c72d1b8a51bd2b5cf91984c`

```dockerfile
```

-	Layers:
	-	`sha256:cc1e9da7a5bdbb3df070b281b5d1b3fb6d1946c9597c66d15ec76e945a264352`  
		Last Modified: Fri, 16 Feb 2024 19:51:52 GMT  
		Size: 175.9 KB (175880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f143a669ab381d6583e54d2f5d8b4b5e2af5e29873cdb6513e275297f35e38`  
		Last Modified: Fri, 16 Feb 2024 19:51:52 GMT  
		Size: 20.3 KB (20299 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6de6b5e7cdea203b5b790800a5bb987c653ab311445edf19f64b5b81a5774a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12714697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bc62fd3591d3f43a8b5f4af67337316df11a6478ee6b5137482e30c49e8181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_VERSION=2.9.5
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.5.tar.gz
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_SHA256=32b785b128838f4218b8d54690c86c48794d03f817cbb627fb48769f79efd59b
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 16 Feb 2024 00:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
USER haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562ebb05af8ae069f087bcc9e91a066e4f2b4cac2721a591b77d7fcc503aa75`  
		Last Modified: Mon, 12 Feb 2024 22:41:20 GMT  
		Size: 286.8 KB (286751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d6fcf4017a80ca60bfd78b795af26fae6f2291641f6c9f6f5451f0e6a5dcd`  
		Last Modified: Mon, 12 Feb 2024 22:41:20 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7624d385bd90f1eb5e9c5c280e106cf7e21e53c6c8b230f32f20655271c069`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 9.1 MB (9067863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f781ce9dda4fe76be624d8116502a24ea8fc27f698a8435993e257e0b199af`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:e745443ef728ef6cef82035b0490c21cdf287c541121119f90958d5cb94a5fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e7f4e421be4928efbf5557ee1d5db2fccb00878d089c4620eaa93540a53277`

```dockerfile
```

-	Layers:
	-	`sha256:c721ede3a2f7079e880b60111bab9e9b6b4c1113f756132621cc043ca288ab66`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 174.0 KB (174007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a56535225cb5cdf6ece0ba8a73eb9c8a6b3a45aff9e5e799ac76d8070d2a13`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 20.2 KB (20231 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; s390x

```console
$ docker pull haproxy@sha256:0f8a0c2e96809db9ce51894817e9b5ecc1136fa0dcaf16d536886a920982a6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c0acdf768bdd4c55ae0a57407af879770cfa8b274ee6a2bcefcf95b736a0ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35065c1af70729689007d4a8937de5c3c422f8a4752673f9a014c1b0442b94f`  
		Last Modified: Sun, 28 Jan 2024 07:22:08 GMT  
		Size: 285.1 KB (285098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33731b789b7e727202c90f8661ab8d0fc2ec15106764b2e97a75cddc289f4940`  
		Last Modified: Sun, 28 Jan 2024 07:22:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a149e4fe8991d42d053f4855f4d3421e7f66eab670b07fa1e318b9ae2345741a`  
		Last Modified: Wed, 31 Jan 2024 22:21:12 GMT  
		Size: 8.8 MB (8781504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe02c6215a65e4aa0a56927c4a81ee7c35c27a4022f27940265cce8e88323a6`  
		Last Modified: Wed, 31 Jan 2024 22:21:12 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:99b983a7c00b12115ef064f6294fe417dc9971b23582127b9f6613b35d58dfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 KB (170288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b05b690fe501c6a7e87d7407608777555f0971b4260c2372949698692686aac`

```dockerfile
```

-	Layers:
	-	`sha256:80a80d5ede856d642e864f262a324f05bc51ea3b2689e78e2ac6b41d8e360dcb`  
		Last Modified: Wed, 31 Jan 2024 22:21:11 GMT  
		Size: 150.1 KB (150111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefc7fc5ab40a67cd6aeaaab8883ca952a15befaaaf10ae1a7cc874989d24298`  
		Last Modified: Wed, 31 Jan 2024 22:21:12 GMT  
		Size: 20.2 KB (20177 bytes)  
		MIME: application/vnd.in-toto+json
