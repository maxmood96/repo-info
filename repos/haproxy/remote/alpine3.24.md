## `haproxy:alpine3.24`

```console
$ docker pull haproxy@sha256:f5437564f819793be4614085ee0bafae45d0579fa2b97f9c76449e60436476e0
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

### `haproxy:alpine3.24` - linux; amd64

```console
$ docker pull haproxy@sha256:6643dc4f99736623733418687925ea209191077884d6091ca6a81ca7ea29082e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20416914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3e383a8851733bfb6b6ff2fda4f217733bcaf79f37f8d0a0854c72f6848f6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:12:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:12:49 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:13:35 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:13:35 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:13:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:13:35 GMT
USER haproxy
# Tue, 16 Jun 2026 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0621a50389929a81602808a824b6b2dc5442fc46eeb7059bbd75cab73a9a05`  
		Last Modified: Tue, 16 Jun 2026 00:13:42 GMT  
		Size: 786.0 KB (786016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb8ba57dbb9e75e8f8b527b376a107f73c308c69fe5c157cbb3ff05e88a9b7d`  
		Last Modified: Tue, 16 Jun 2026 00:13:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82ee44a4d49985584ab760f22a8588ef8ccf7e24f1e9fea4b526eb54a60af2`  
		Last Modified: Tue, 16 Jun 2026 00:13:42 GMT  
		Size: 15.8 MB (15783073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b54748b1ffd61065cab8ca29795cbee8a5e4bd6a1b8b62f03bc869fd9731c6`  
		Last Modified: Tue, 16 Jun 2026 00:13:42 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:cc31a7cc8c785cd3aae4a119869a15eb87eaac8f11701ca46082617875ace8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 KB (230808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6575550721774c8793acf4a35abb0f81425c5bb345bae940a28721271cbfede6`

```dockerfile
```

-	Layers:
	-	`sha256:6ed45f17f9d0469f1eb71fe3c0094a4403cb3d9bf268dd9e59b0f7af9dc0d89d`  
		Last Modified: Tue, 16 Jun 2026 00:13:42 GMT  
		Size: 209.0 KB (209015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4315858624745c54cadc10af12ea5d80d9e5696ea005b91c68aec3607982c8a0`  
		Last Modified: Tue, 16 Jun 2026 00:13:42 GMT  
		Size: 21.8 KB (21793 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:05f9dc297a5c254c2aa3382b0797848288ac72443478d7a8e7afa92d1739016b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20367998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e074e2fd2a88525c27e9f00c8cd3270fc7ffda1974c3c9c800f7b0da6127fe36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:10:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:11:32 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:11:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:11:32 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:11:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:11:32 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:11:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:32 GMT
USER haproxy
# Tue, 16 Jun 2026 00:11:33 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:11:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb987b4d942477be920479244c6d561e6a359538accbe0eb947266e2306f5c2`  
		Last Modified: Tue, 16 Jun 2026 00:11:38 GMT  
		Size: 777.7 KB (777663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a65be69eafb7375a502b9036c000faef8bea44d268d8a6510928a17eef213a`  
		Last Modified: Tue, 16 Jun 2026 00:11:37 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcf6bdea34c3454dc291881d5d5eebce6a0d17c20e32876da5236af7a2f2e6d`  
		Last Modified: Tue, 16 Jun 2026 00:11:38 GMT  
		Size: 16.0 MB (16035449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2509286ee87767368788e17a1132041d8b6444b0120a26a572ab3ea5e5e02f66`  
		Last Modified: Tue, 16 Jun 2026 00:11:37 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:98b7573f19eaee62f9f9e64b8379bc0c11348b8be057328e470ba8b0f0530da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d09bb8df66530dfbfd6c319f9387ca5ea5c0053ad91498978e722cc5f1d67dd`

```dockerfile
```

-	Layers:
	-	`sha256:b952791bd4ba997e16badbe7b3c8683b77cdf50257983267c1cfe517d34ac1d8`  
		Last Modified: Tue, 16 Jun 2026 00:11:37 GMT  
		Size: 21.7 KB (21716 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:39948899d749544619acd0e9cbe1a58c2faf2c2e354a32ca17eb3d9a61cf2460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19864219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6009d61e9fcc404332ed56018c3190e66293a76adeba520745bdc441d170c231`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:13:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:14:25 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:14:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:14:25 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:14:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:14:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:14:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:14:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:14:25 GMT
USER haproxy
# Tue, 16 Jun 2026 00:14:25 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:14:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ff1fad000e56678fa646f7b463feb26e6e8e426f420abbeb441b10d30c7e3d`  
		Last Modified: Tue, 16 Jun 2026 00:14:32 GMT  
		Size: 732.3 KB (732268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3059b08b305947fb2545b12ff7bc091afd69741b029ae1ef5fcedb6cd6add`  
		Last Modified: Tue, 16 Jun 2026 00:14:32 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e61494047139c0e4f9cee52c73bad7a83768cdd8bd6ea6e9f4e387384acdb4`  
		Last Modified: Tue, 16 Jun 2026 00:14:33 GMT  
		Size: 15.9 MB (15869900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8b9b94092e117bff23b4630bcde455eb1def632ef0baf92bed503d35d7c886`  
		Last Modified: Tue, 16 Jun 2026 00:14:32 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:0067ce47e4d93d1c89217e8b74f4c51b9663bcf51736c2c20cbe1abb529ee260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588849d8934f54306e2bea9053ae219af8a4a9b34aba9171df9d914856dc2807`

```dockerfile
```

-	Layers:
	-	`sha256:46a717de67c20747ac4cdf3438f459d75ad8f8965d9195b18b219fb125f80309`  
		Last Modified: Tue, 16 Jun 2026 00:14:32 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fae99d7c3bb8ed2b26e62416edcf921de1fa0c5710439a9168881460418945`  
		Last Modified: Tue, 16 Jun 2026 00:14:32 GMT  
		Size: 21.9 KB (21931 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b61dd22febb50a154ac8b8c4aba821d74cc558a011b19e90f998099ea7f6ceec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20528697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787e094fc641def2d8f74346178cd70752383b23f637171be7927ac87126d397`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:13:00 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:13:43 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:13:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:13:43 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:13:43 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:13:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:13:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:13:43 GMT
USER haproxy
# Tue, 16 Jun 2026 00:13:43 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:13:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4682fda6113475496c6db096d3e15b8d36b21c53e9222204ecb1981e9fa03801`  
		Last Modified: Tue, 16 Jun 2026 00:13:48 GMT  
		Size: 799.2 KB (799190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6bf092157a981b0b846aa8fb494ab8e06665fbb90ad8135615d7fd5f0c7f48`  
		Last Modified: Tue, 16 Jun 2026 00:13:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b411558345ad92f7440e4c8a7b546bb422dcfeb711e54245be3ab843dfa536`  
		Last Modified: Tue, 16 Jun 2026 00:13:50 GMT  
		Size: 15.5 MB (15545036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523271ec285b7b5e72bdd978ad6f68774bb8d5bf4d1f95424399a8b35e18530e`  
		Last Modified: Tue, 16 Jun 2026 00:13:50 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d77037648af7ae1163e988cb14f7be29937c2aa19c91ca1c252c753854f1013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c6ac22e433cd939c8a3adc5072d4746eda94d4fd492cf7821c04cfe6ba02b0`

```dockerfile
```

-	Layers:
	-	`sha256:1368443443d317de710a75dac78971e6c1cfcdbe5333df91fcec14eb42524538`  
		Last Modified: Tue, 16 Jun 2026 00:13:50 GMT  
		Size: 208.5 KB (208469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e76e42661ea51d9b7ec3d1d81b2a07c40aca2350d9fb2d0dacf0bf5ce470210`  
		Last Modified: Tue, 16 Jun 2026 00:13:50 GMT  
		Size: 22.0 KB (21975 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; 386

```console
$ docker pull haproxy@sha256:832985b52112d3de9fe112b3cb0b88746fbb47c12ea7b9402f2f4122d9f7a715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20028198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0037f9af20cb4714d32d76f62944e05073e1d2a67cbc73cf50fc07f4880210a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:12:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:12:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:13:13 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:13:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:13:13 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:13:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:13:13 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:13:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:13:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:13:13 GMT
USER haproxy
# Tue, 16 Jun 2026 00:13:13 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:13:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b99539f179e63ea7653a4758c2a46cf8f3d870d6d5a452d515cfa23a118c3`  
		Last Modified: Tue, 16 Jun 2026 00:13:19 GMT  
		Size: 790.9 KB (790894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2961146facfa982a048425728a4e23b0f571fd42691ec0864d14d6c6ba9fa1d`  
		Last Modified: Tue, 16 Jun 2026 00:13:19 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926bc7d97b76d707f7daf4530f0fa93a9a8c8728f5584449a55994db29e309c`  
		Last Modified: Tue, 16 Jun 2026 00:13:19 GMT  
		Size: 15.6 MB (15565727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496a2233da251e8b69b57fa0265e10796a16fc1a20542d50c8d83c1b29dd7a03`  
		Last Modified: Tue, 16 Jun 2026 00:13:19 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:e8768a7a58128d70001746419f6f4bf83480bb9394f2f1d4d5f148d7eed55c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 KB (230707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10b9aef2583dddaaa5e2564d0a2b2fd48f8449f0de0592f839eb56b2bcfb977`

```dockerfile
```

-	Layers:
	-	`sha256:6a03c2b50af3dd80bfe5fd4a143993ab137617755f02ef0b212ee8fa778fde77`  
		Last Modified: Tue, 16 Jun 2026 00:13:19 GMT  
		Size: 209.0 KB (208970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1a2153a9cf2d9ca15f2964e41652be195a930da64503802575f466c45e7ecd`  
		Last Modified: Tue, 16 Jun 2026 00:13:19 GMT  
		Size: 21.7 KB (21737 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; ppc64le

```console
$ docker pull haproxy@sha256:17df7a601006ea52ec17f77a5ac2120869d8fe5691a2e8269d19af73899cdce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21243999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7643b1bf347bcc216aeece863b2635a66224c162071644f7ef30e27fef7eff08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:10:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:12:04 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:12:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:12:04 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:12:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:12:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:12:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:12:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:12:04 GMT
USER haproxy
# Tue, 16 Jun 2026 00:12:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:12:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d7eda7c30cfd9220352932d2fab26c0a09ec13e630c5cfa190a8d667b639a4`  
		Last Modified: Tue, 16 Jun 2026 00:12:17 GMT  
		Size: 820.8 KB (820835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08361da2f18efac83dabb6c40b81b2c6459e8373f02643568e9e7905eaaa001d`  
		Last Modified: Tue, 16 Jun 2026 00:12:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a681d4fd22fd53d0fb704c6e921ddc9b62bbdec4a921669fa8cb6eb5b306d24`  
		Last Modified: Tue, 16 Jun 2026 00:12:17 GMT  
		Size: 16.6 MB (16608325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cbbed054bd4a8fc97c4d646308415b11d23e293cbefd49b6ff43a81f10e350`  
		Last Modified: Tue, 16 Jun 2026 00:12:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:1faaff54ac758c40dadca454cc2ffbcf7dd22a5631f22e8e3486e362c9dc5715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 KB (230287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e818fc2278978e21440611a0dd43c62df7221f03dc76782d96851a3ccc1b2321`

```dockerfile
```

-	Layers:
	-	`sha256:068e6b640113751e92062f5b41c9a9cb8a06e59346f4bfd76c5bce6ef3d3bd9a`  
		Last Modified: Tue, 16 Jun 2026 00:12:16 GMT  
		Size: 208.4 KB (208422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60f36f064f6922944cd62cdd345c22285fc694c2bd4b35b0d2141bc9775be2e`  
		Last Modified: Tue, 16 Jun 2026 00:12:17 GMT  
		Size: 21.9 KB (21865 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; riscv64

```console
$ docker pull haproxy@sha256:e84eb5f3dd79d6dbdd06e179d5c251df818874ef1992cd7201cdc69b5f9c74b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21380088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab08d71541b5dd66e713d41b61b788c253e0a7e52c4df729e65a5229a7fe0a62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 09:14:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 17 Jun 2026 09:14:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Jun 2026 07:17:39 GMT
ENV HAPROXY_VERSION=3.4.0
# Fri, 19 Jun 2026 07:17:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Fri, 19 Jun 2026 07:17:39 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Fri, 19 Jun 2026 07:17:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Jun 2026 07:17:39 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Jun 2026 07:17:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 07:17:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 07:17:39 GMT
USER haproxy
# Fri, 19 Jun 2026 07:17:39 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Jun 2026 07:17:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0e4b27bc76910fa0eb8988c9b1c0d6494b84ba811d1f4336ac9ec50e60576a`  
		Last Modified: Wed, 17 Jun 2026 09:48:17 GMT  
		Size: 805.7 KB (805698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7400c12caf29c98608ef5d6aea6c1ef4d39861f7657de269fbd138bbe5cb756`  
		Last Modified: Wed, 17 Jun 2026 09:48:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e04188ae04a59aab6c4012fbfe32e92d0653f03e6311b83c7b1b1405832817`  
		Last Modified: Fri, 19 Jun 2026 07:18:33 GMT  
		Size: 17.0 MB (16998587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c23db1d86f3610937eec3b56dc03ef3022af8c7aae08c0c5f7b92b5d4513078`  
		Last Modified: Fri, 19 Jun 2026 07:18:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:434744de66868772e4f9de6a79a0495ee94ad2e83822501e0bf726b676bc3d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 KB (230282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2356eb77de0547d13de65604d15f6970fa91b556601288ded28d9c7c0e8b87`

```dockerfile
```

-	Layers:
	-	`sha256:5827f9ec02c8db512608a6fddc926eabe26397f69ad1f2cace4c2178f8eb00e8`  
		Last Modified: Fri, 19 Jun 2026 07:18:30 GMT  
		Size: 208.4 KB (208418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f3ad3c0c4f6d712dae63946f70e5aa2e5b87da9d23671f9ae2a5bf2540785c`  
		Last Modified: Fri, 19 Jun 2026 07:18:30 GMT  
		Size: 21.9 KB (21864 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.24` - linux; s390x

```console
$ docker pull haproxy@sha256:7a49dc6d309a66ab36a3f6d65bb896634220bb2ad63bb38c48763e1a7b9e05c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20765680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364ded3ee09bd2dd2e1aafdb9e901b27b9a98b486c3d208e9041751a728f276a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:10:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 16 Jun 2026 00:10:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 16 Jun 2026 00:11:46 GMT
ENV HAPROXY_VERSION=3.4.0
# Tue, 16 Jun 2026 00:11:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Tue, 16 Jun 2026 00:11:46 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Tue, 16 Jun 2026 00:11:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 16 Jun 2026 00:11:46 GMT
STOPSIGNAL SIGUSR1
# Tue, 16 Jun 2026 00:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:11:46 GMT
USER haproxy
# Tue, 16 Jun 2026 00:11:46 GMT
WORKDIR /var/lib/haproxy
# Tue, 16 Jun 2026 00:11:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aafffee4232a61a5a0515622c05c542ba8aae45d132fd075016a77165701cb`  
		Last Modified: Tue, 16 Jun 2026 00:11:57 GMT  
		Size: 848.8 KB (848824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d090c7782239f59acd50254089552967b6b775d4e2ea5c2ad34ef534d4c1846a`  
		Last Modified: Tue, 16 Jun 2026 00:11:57 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a797458ec5b90ed72fa0e3854655bdc0999ae945b23223adddf632f28cf5f5c`  
		Last Modified: Tue, 16 Jun 2026 00:11:58 GMT  
		Size: 16.2 MB (16206097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59edd6ca5277ee0e398768021f51a39625a9ac5876e80af5c76621c7a5a47d`  
		Last Modified: Tue, 16 Jun 2026 00:11:57 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:90a821e72a09a23a7281aee7a41e4692c9365069ff23989cf88399a96a2c8aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 KB (230157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a383e844db2e8b3f76ffe5c19912984aa1603f1d108d676c322438d02e3fbc0`

```dockerfile
```

-	Layers:
	-	`sha256:db1339be8922a7651de3f71bc629b2f14495780076934613142813f853944cfe`  
		Last Modified: Tue, 16 Jun 2026 00:11:57 GMT  
		Size: 208.4 KB (208364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b220424f19ec43a01be811b647a785fde6b47d1865e6bad65f6aebf4c6b3a`  
		Last Modified: Tue, 16 Jun 2026 00:11:57 GMT  
		Size: 21.8 KB (21793 bytes)  
		MIME: application/vnd.in-toto+json
