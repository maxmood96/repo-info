## `haproxy:alpine3.23`

```console
$ docker pull haproxy@sha256:d3b50f8bc0121e49b47ce4118571da140f8a62b38f6ca011b66ebfd09750c87a
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
$ docker pull haproxy@sha256:b7ea779d1d813a60492f9af47c0098aeee30858d1dc9d72d2770bfe8cf36d951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19111044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342386066bafdab584fc56e05a5cf70d81b11d9cfdc13e87f0437311017cdde5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:02:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:02:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:03:32 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:03:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:03:32 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:03:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:03:32 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:03:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:03:32 GMT
USER haproxy
# Fri, 09 Jan 2026 18:03:32 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:03:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280cdb29719bb3b9e56d7a77a6565a15793537443fd2e66d809aefefeabbb08f`  
		Last Modified: Fri, 09 Jan 2026 18:03:39 GMT  
		Size: 829.6 KB (829633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2103c42195a38131e351c7b95ca936d54e38f979fa7c7b16d9eb49bde3e0ae7a`  
		Last Modified: Fri, 09 Jan 2026 18:03:45 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04500063db4848ea9d81f0fcc60bbac511e9d8432fdc13c0c6e76715d66e5367`  
		Last Modified: Fri, 09 Jan 2026 18:03:47 GMT  
		Size: 14.4 MB (14419871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a11d7580115f621e128374d60023078b06ffd0da57a5f7bf10cbfe0cf79a71`  
		Last Modified: Fri, 09 Jan 2026 18:03:45 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:ba82aa47a1aa98f672706a34de72a0f7e2262512845edfc80de9e15f8a9c5f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 KB (248475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e993f65d97bb4a9d181c41380d45ab94c332d9d11cc5d094766bfa82cd2ff3`

```dockerfile
```

-	Layers:
	-	`sha256:abfb22ae82c9ee26d4123a8d5095fd1cdd71e4bc41cf82b8f3c216d0caecbe47`  
		Last Modified: Fri, 09 Jan 2026 18:03:39 GMT  
		Size: 227.3 KB (227306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02784d87eda5304214d6516a655ebb0762a9b0ed01a911901285bd8d969880a3`  
		Last Modified: Fri, 09 Jan 2026 20:03:01 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:8aa1e304d54d87a983e50aca912c0ee9e8a8e2accc9293aad89b173f8c34610a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19032553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1422b7f2eaae3147cf6796d40ca066c4c444909d375ddb4ba41333e27bd6dbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:02:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:02:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:03:39 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:03:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:03:39 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:03:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:03:39 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:03:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:03:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:03:39 GMT
USER haproxy
# Fri, 09 Jan 2026 18:03:39 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:03:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b93148847731009d98758d28d6e4102b862038e1eaba02acd763e708db722`  
		Last Modified: Fri, 09 Jan 2026 18:03:51 GMT  
		Size: 821.8 KB (821847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeea952586ace65248f76934771d55598d61c0f8431883556df3010fd10f1acc`  
		Last Modified: Fri, 09 Jan 2026 18:03:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c91dd5b1b2a6c5a3b8578ae500427491f1975cb987297aad2e9772503ea76f`  
		Last Modified: Fri, 09 Jan 2026 18:03:52 GMT  
		Size: 14.6 MB (14640839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c47bb4d80408923ce9e35ef33226e8bfc6944e5ccf465abdbb0c07eff904ea`  
		Last Modified: Fri, 09 Jan 2026 18:03:51 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:f7674d6be252a82d4bd812f99851ef8e7131b57fdde7da5f38cf32d447e4bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6142bd6b353f018f1d58f7f17d6704ee22f18959169d6a33a4de70cce1a1f0db`

```dockerfile
```

-	Layers:
	-	`sha256:065d6cc022d1e02d8f8035ddb7e9c580e2d1f17c9c77af42c8a35a2eb7cc0f93`  
		Last Modified: Fri, 09 Jan 2026 20:03:05 GMT  
		Size: 21.1 KB (21076 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:9bf4887419c56f1fbb72ac284d587fcac3fe75428d2ccbd839aa80ad65a8a691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18549184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7df8dc9836eead4df29b8fb243a9d9fcf505aaf564bf0af078cb01bc648ae9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:03:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:03:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:04:33 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:04:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:04:33 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:04:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:04:33 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:04:33 GMT
USER haproxy
# Fri, 09 Jan 2026 18:04:33 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:04:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5316a79d01fcf66f1bb738c8771b15b71f08fe3fa619228323de14429b0d7d`  
		Last Modified: Fri, 09 Jan 2026 18:04:45 GMT  
		Size: 777.7 KB (777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91c26a790cebd6d8af909f89f0616396de3b0e84a7ac4458bebd0808cae4fe7`  
		Last Modified: Fri, 09 Jan 2026 18:04:39 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315b989cd600587065e0660ccbbb4de8bac637e89e030c01e7182b11e58a64ba`  
		Last Modified: Fri, 09 Jan 2026 18:04:46 GMT  
		Size: 14.5 MB (14490626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353698b2a9fd264d1ee5e460392e9fa4752cc1d431f02eb5d37e9b4882bfe1f5`  
		Last Modified: Fri, 09 Jan 2026 18:04:39 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:df13556820dd999ad66b1c53d8bd493010cc58b04a965aaa2fd9ff8caf6489db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa89293b47da96be7860480684e9876756ae7a42e93671b7c206f2d275d3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:42b89f9f65f1b663d1c721231e2e03138447a7e49e4fea55761689cf453ed9dc`  
		Last Modified: Fri, 09 Jan 2026 20:03:08 GMT  
		Size: 226.7 KB (226708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684ff5f53fa1fcaafe4c8ace7aa33bd3314a3ee5189cfdea4833e7e2e6a40dde`  
		Last Modified: Fri, 09 Jan 2026 20:03:08 GMT  
		Size: 21.3 KB (21291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:8d7b821ab366ca2b8ed58de7eef68c07858642d2c719ad313ffdc919650a36fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19207142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18df96754ffb9572c9c9666286a282d543044cede5fd0b23057903bc1f3b8e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:04:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:04:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:05:15 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:05:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:05:15 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:05:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:05:15 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:05:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:05:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:05:15 GMT
USER haproxy
# Fri, 09 Jan 2026 18:05:15 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:05:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d0245d27a0cc0b2f9beee1bf984f8fd7a27b29167c873ba18e5f90ad842ac`  
		Last Modified: Fri, 09 Jan 2026 18:05:17 GMT  
		Size: 842.3 KB (842337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b3972e39449e5ff3bac83f7a41cd3edabdfff10451d960c5c39ec99187a48`  
		Last Modified: Fri, 09 Jan 2026 18:05:17 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12af782f09f83fb1e6fef2515faaa385ac0b8ed7943a66805a50acfd7d7414bb`  
		Last Modified: Fri, 09 Jan 2026 18:05:30 GMT  
		Size: 14.2 MB (14167623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a861272283dd5ff742f642b86ffcd066a01374f7562ad6b8ea7cba76a7ad92fe`  
		Last Modified: Fri, 09 Jan 2026 18:05:28 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:068623cb4e9d8387b34517cdc110de3fba9e970246d2c4f498b09a8c490945b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 KB (248062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5dfac2a80b999403229900650fd44ccc22dcba073be7e8ac622240f5451862`

```dockerfile
```

-	Layers:
	-	`sha256:4ceece31d2d10bff50bd02d9aab642e837799526649c19f08cdfdbb610eb05f2`  
		Last Modified: Fri, 09 Jan 2026 20:03:12 GMT  
		Size: 226.7 KB (226736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393350864caefa8372f9ffb9b2b06ccaeba36e264d924094c0ffe276817fe04d`  
		Last Modified: Fri, 09 Jan 2026 18:05:22 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; 386

```console
$ docker pull haproxy@sha256:8ee5fa26f40ef0f82b224a35b2863ba06b0414044d17d392ef184fdd048ec651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c857f3e0631df58b8b998bed96d9ea4c40fd7b186588d8cae9dfcf74b9cb25cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:03:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:04:18 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:04:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:04:18 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:04:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:04:18 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:04:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:04:18 GMT
USER haproxy
# Fri, 09 Jan 2026 18:04:18 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:04:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e763f4d9443b207585502ad7fd71d5113bf371d4b9e32c63c5ba40b0b6dfd2`  
		Last Modified: Fri, 09 Jan 2026 18:04:09 GMT  
		Size: 835.9 KB (835936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828fd1c6c248652ad58ec66ebe849d853bc8a342c1d33ad70f23cea64843f015`  
		Last Modified: Fri, 09 Jan 2026 18:04:09 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71be0649c486df8516592c7d421e22118f155d691695be265758595b92e69f2`  
		Last Modified: Fri, 09 Jan 2026 18:04:26 GMT  
		Size: 14.2 MB (14218008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73137267134a19af2b1f93085aa6a08f61eaa34a8361688b653dc34c2cd1cb04`  
		Last Modified: Fri, 09 Jan 2026 18:04:25 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:cda429c99503b2e448cc3fa44e6113e47f1fd8163848551ec00e3ab8309e466c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 KB (248394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee3233735db38b29379d0b0714925a1863f2eb71a71d571c4ee72e98806f696`

```dockerfile
```

-	Layers:
	-	`sha256:618804f2462d2dd7efd4fe7910e5ed14a42dbc309badab36a13826aece076a1a`  
		Last Modified: Fri, 09 Jan 2026 18:04:25 GMT  
		Size: 227.3 KB (227271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0fdf162ad1ecda92913dc4361889bda388f7b99e95bc0635a80019dd8aab58`  
		Last Modified: Fri, 09 Jan 2026 18:04:26 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; ppc64le

```console
$ docker pull haproxy@sha256:681acc168be2c3d1395ea1f2912a1a6bda8d9f5ba9ba91ec44488e6845e96875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19887502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07ed59c4d00313b82d348eec0be83fe99d6ea472cebee9d44abfee6592eafed`
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
# Fri, 09 Jan 2026 18:04:25 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:04:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:04:25 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:04:25 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:04:26 GMT
USER haproxy
# Fri, 09 Jan 2026 18:04:27 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:04:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
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
	-	`sha256:a9331d03f3cef7a176ddcc68ce1e3b3230ed173d29d3dc8d60851f41f90d5105`  
		Last Modified: Fri, 09 Jan 2026 18:04:52 GMT  
		Size: 15.2 MB (15192498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750f58e3356e5c7c993bb0aedeaac95ea011010586884e70e3aae913723546e0`  
		Last Modified: Fri, 09 Jan 2026 18:04:51 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:10a2eb7373e6041d8383f80cac7ed5dc8f39ce8c59684be8459b171d0c99fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac264b851d51173fd85f8d5bf5747492624db5802e706f612d43b67d5de2c13`

```dockerfile
```

-	Layers:
	-	`sha256:28e0224eccddfce178ef50c640bf837f593a831602e493347609eec6a0d5d02c`  
		Last Modified: Fri, 09 Jan 2026 20:03:20 GMT  
		Size: 226.7 KB (226701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f479a86e0ff58a3382a2979bc617a6de76480507b9901455cf374c9550cfa819`  
		Last Modified: Fri, 09 Jan 2026 20:03:20 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; riscv64

```console
$ docker pull haproxy@sha256:47cc276689f888e9de5a9008ef9ab0a0441543a288cb8aa8264a8d1e7d6fb562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19995579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed8688592a9558a6aea5c2a1d9a62be02fa2e107cb4bbc5aa9beb62f7e4f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 05:00:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 05:00:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 19:09:33 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 19:09:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 19:09:33 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 19:09:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 19:09:33 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 19:09:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:09:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:09:33 GMT
USER haproxy
# Fri, 09 Jan 2026 19:09:33 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 19:09:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac202a4ea053c559abb0839547921026b5c60ef3268d982da82c523fc6ec02b5`  
		Last Modified: Thu, 18 Dec 2025 05:15:11 GMT  
		Size: 849.9 KB (849928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2942b29757a2f3be1a51fbe0d838f5da7e1811a07e28b7e01723666deab1f454`  
		Last Modified: Thu, 18 Dec 2025 05:14:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c095678fd453d5af7bd46459e0231fd74ad840edaccade08f6c1e81cecd141`  
		Last Modified: Fri, 09 Jan 2026 19:10:28 GMT  
		Size: 15.6 MB (15560269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6daf6296e7e9154ecc193e7c26de4a7cc5baea5c04bfd7800581eb20165afc`  
		Last Modified: Fri, 09 Jan 2026 19:10:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:b8f245a0c0f60d671237ab9dec3bba08e863a6f74424232e28a9dc55dd9b54cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0a253fa4167c797c6bb22746dd1bc0582e93f370226e10e39586e6712556fe`

```dockerfile
```

-	Layers:
	-	`sha256:4b4133ce8ae434339fe8fbf64cea097ca7cad99ba6ef6b8770e270c8cd20c2bf`  
		Last Modified: Fri, 09 Jan 2026 19:10:16 GMT  
		Size: 226.7 KB (226697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80465cc77c6094179eb0a0a6983463726860b279660680cfb45fb25eccdab96c`  
		Last Modified: Fri, 09 Jan 2026 19:10:16 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; s390x

```console
$ docker pull haproxy@sha256:9df2359023b458450f0a340a6638f2fc9905ca186889d54aaae9d4b3c112ba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19416456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64f0635f68e5a6ecd76679c8a58f3a80d8e2b41e33e1defc60a15ea9ddd56d6`
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
# Fri, 09 Jan 2026 18:03:05 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 09 Jan 2026 18:03:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 09 Jan 2026 18:03:05 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 09 Jan 2026 18:03:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:03:05 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:03:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:03:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:03:05 GMT
USER haproxy
# Fri, 09 Jan 2026 18:03:05 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:03:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d72f959e55ce0a0ba7077382dc97d683e56c7d1901d55abcae919e934370a`  
		Last Modified: Thu, 18 Dec 2025 00:27:28 GMT  
		Size: 891.5 KB (891544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c5385c88d82e1ab96c9fcdcd46f6cfdcff7ab2a864621ca280f82cbc067465`  
		Last Modified: Thu, 18 Dec 2025 00:27:28 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d133519402d1ebb97a933d5ae4a09aba6972ee1ccfcff321c6303d97afbc67f`  
		Last Modified: Fri, 09 Jan 2026 18:03:16 GMT  
		Size: 14.8 MB (14799166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f243d64515ae38c9bc53e74c919e2df2bdabf4f6d6a25598f683b63c51248`  
		Last Modified: Fri, 09 Jan 2026 18:03:15 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:f36b3438e58d924234d2b06b88a9f9f6886247fbe9fd32a179913362a444f01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c875e3fee37c74381025ed640308100938f5e5c8805a10d69d3c7fb2a5c044`

```dockerfile
```

-	Layers:
	-	`sha256:432c899dabf914dc79e08f9131452aff3b0e11a00fa2373fbe5fffcf1028424e`  
		Last Modified: Fri, 09 Jan 2026 18:03:15 GMT  
		Size: 226.7 KB (226655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768f19c14a6810a70e8ae648bff099930db2e86f56740e24935753f647a8f9a3`  
		Last Modified: Fri, 09 Jan 2026 18:03:15 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json
