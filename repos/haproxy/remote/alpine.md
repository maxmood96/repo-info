## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:e5f8007537729de9be55c843a884145d7020ff165a36aeb88b3b46d31cac8e9e
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
$ docker pull haproxy@sha256:0797f2f0cdfe70a0156a8faa54c9e9d9052a72ce5918cd498e2875915f06ca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19118746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dbc2acc5282c1113074b5677fd5b25148457470082fcca92fbe448b6784593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:48:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 12 Feb 2026 21:48:36 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:49:26 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:49:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:49:26 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:49:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:49:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:49:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:49:26 GMT
USER haproxy
# Thu, 12 Feb 2026 21:49:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:49:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ff410af4c65240fc525d34844ac391faae35709b0c7cd1d6ac271cea55367`  
		Last Modified: Thu, 12 Feb 2026 21:49:33 GMT  
		Size: 829.6 KB (829615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc06be102be453483d5759149784ff5f1bc92cd94e57fb6d4cfc825285ef422a`  
		Last Modified: Thu, 12 Feb 2026 21:49:33 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c9a13402627922aa0fdcb9bced8d211297c07c14eeefc961ffc979f36619f`  
		Last Modified: Thu, 12 Feb 2026 21:49:34 GMT  
		Size: 14.4 MB (14425872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6a15b0565bebebcb263248ab7b66b48e876134f72c132b93ec429cc526bce5`  
		Last Modified: Thu, 12 Feb 2026 21:49:33 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:32b15f6795dd02b1773df019213b3c557ed44f0ccae9872d2c7f24f6e0d9899e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 KB (248475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b4b4e77e9db0bc398f86efeb34521705f21eea6ff905ef30335ae1f290d0e0`

```dockerfile
```

-	Layers:
	-	`sha256:b0d4a37cbb564783c4c9a12834bfee8c520d870f06330ca1336d65ecd8c59545`  
		Last Modified: Thu, 12 Feb 2026 21:49:33 GMT  
		Size: 227.3 KB (227306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e414bd2a1cedd6cb67b29aa970f22467b2ae76186b1e178cdc55eacc280d03`  
		Last Modified: Thu, 12 Feb 2026 21:49:33 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:f0da06d3d53db9db1ae5d0b749facf07578b6d564b3380b7f6fe0e45780b4bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19050402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77093dea5a8da62883b78e1229888b23e393615c501a57c4b8035b54cbe5e09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:46:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 12 Feb 2026 21:46:21 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:47:07 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:47:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:47:07 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:47:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:47:07 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:47:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:47:07 GMT
USER haproxy
# Thu, 12 Feb 2026 21:47:07 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:47:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2516c3a895ded02cd77da47bce78e9db9da0cb5ac0d702cb2e8457532017aa`  
		Last Modified: Thu, 12 Feb 2026 21:47:12 GMT  
		Size: 821.9 KB (821853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6eb53e37433d47b83b216f216fed8a899aa62bd82df8613c712b43f598eb98`  
		Last Modified: Thu, 12 Feb 2026 21:47:12 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0f5df227b4d988c8c7e2d4eadc436f2c1bc4f5911d6b6203c259cb78ebd900`  
		Last Modified: Thu, 12 Feb 2026 21:47:12 GMT  
		Size: 14.7 MB (14657289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf732526a5bd8d402cb05c58463d8116a0a7021debee6fcbf5db9afa172ee24`  
		Last Modified: Thu, 12 Feb 2026 21:47:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:e2f7acc693574d3bbe65033a94af077452fc98a2c86314f35078a99b1ee17a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e8ef748bafee68f261426519a0814f66bd8bc55f0f5864be381dcec9f2801`

```dockerfile
```

-	Layers:
	-	`sha256:5c16bd720435df15c29280fb49f20d7a38f98be53e189805864ad3c8de22d821`  
		Last Modified: Thu, 12 Feb 2026 21:47:12 GMT  
		Size: 21.1 KB (21076 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:470d9a09a4d50faf56d2f1d48d9dca1535b5696a19778ea7bfa6faeadb982b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18562394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc82ee2bf430bcec19ce71ccab3ef53f38ab4c46ebed80133f66e230d2ee57b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:49:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 12 Feb 2026 21:49:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:50:13 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:50:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:50:13 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:50:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:50:13 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:50:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:50:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:50:13 GMT
USER haproxy
# Thu, 12 Feb 2026 21:50:13 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:50:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda15afaaf6fef7ad7e7e658b0c10f42dd400a7faa46ccd1fda576b68efa4d27`  
		Last Modified: Thu, 12 Feb 2026 21:50:19 GMT  
		Size: 777.7 KB (777730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5da00230d83225cf4eb3604323a48628a1c9b839da4ccd2cfb9f533f719e73`  
		Last Modified: Thu, 12 Feb 2026 21:50:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae2a1666acea4cfb63e7468725fa407d61e9b556bd1e73e2cff33b4a620409`  
		Last Modified: Thu, 12 Feb 2026 21:50:19 GMT  
		Size: 14.5 MB (14501498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b4317a063db1c9116eb69c703ff87a61184a2d2c2aa981fc712ad2364cec6`  
		Last Modified: Thu, 12 Feb 2026 21:50:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b9c40e85933cfa66bbb06844d04b0dcf22b24b98d56f3dceabbc627887df2992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a21cc6c34c094bde41c5df4f7b22cd3cefa0118737fa1d1c43f0e102920da02`

```dockerfile
```

-	Layers:
	-	`sha256:d0030ce583754d6f887cd57cb9bcbb7d6be7ecc8760afd41406f8ef3e2ff0c34`  
		Last Modified: Thu, 12 Feb 2026 21:50:19 GMT  
		Size: 226.7 KB (226708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d537868af8b261ca35faad202e7da502b01ef87f4a0ea7ddc08100c8ea90d77`  
		Last Modified: Thu, 12 Feb 2026 21:50:19 GMT  
		Size: 21.3 KB (21291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3d439d888351c89afb333ecfd2ce16d990d5aefd5efca82d1457902d49357f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19229743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5fce3dbf449c7f68df625e774db7a95909aec225fb88f824a1e99c883e4b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:48:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 12 Feb 2026 21:48:01 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:48:41 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:48:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:48:41 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:48:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:48:41 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:48:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:48:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:48:41 GMT
USER haproxy
# Thu, 12 Feb 2026 21:48:41 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:48:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76143c857c6a619d3958cfa1177b5250f493a8c23783cc4d704795afecf15738`  
		Last Modified: Thu, 12 Feb 2026 21:48:47 GMT  
		Size: 842.4 KB (842366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d6767d866a526d059508fe99bc2ea5ad3b8bec5dfd05e2fcc5c067b5f192f5`  
		Last Modified: Thu, 12 Feb 2026 21:48:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229378725097023558d29fe106a0b49dc0e969d1931ae85c98db1dee78dfd564`  
		Last Modified: Thu, 12 Feb 2026 21:48:48 GMT  
		Size: 14.2 MB (14188851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b278922f2b72cb2beca7771cc93fd8f60469bbda4c258b806d1d6307d714b9a2`  
		Last Modified: Thu, 12 Feb 2026 21:48:47 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:5594a0c1c137bf47a72f88c3ff64e61064a843c92191e09b99176868e5578347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 KB (248063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e40bf02b1025a45b744ed0e51473a80227e8c9ce06f63a10f65242be8758a`

```dockerfile
```

-	Layers:
	-	`sha256:c01f1580421c6ec6f0cb90884bf7f1e15da85d13bfbc1423dc1cee77b3eeadcf`  
		Last Modified: Thu, 12 Feb 2026 21:48:47 GMT  
		Size: 226.7 KB (226736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14e30c657553491a9838901312f46a9313a4595e52eef44b5a1082e7a5291b1e`  
		Last Modified: Thu, 12 Feb 2026 21:48:47 GMT  
		Size: 21.3 KB (21327 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:593a733d9bbfa7c9ba09e6ebee411102b9870472dd725898f1358927f4bc13fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18744885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6b6a58eed2dd0c6cb974cf028f98c7506b7990ee2043e4e5b570de7a9ed171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:48:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 12 Feb 2026 21:48:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:49:04 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:49:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:49:04 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:49:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:49:04 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:49:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:49:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:49:04 GMT
USER haproxy
# Thu, 12 Feb 2026 21:49:04 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:49:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e83b097ba18a3a29fc13f0113992d102348da31589aad08c9e76a3ab1e224c`  
		Last Modified: Thu, 12 Feb 2026 21:49:11 GMT  
		Size: 835.9 KB (835946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e670a760c95b13dbdacaf9f1d4f3475606b5a229d4805b589a3e5faf5a557a9b`  
		Last Modified: Thu, 12 Feb 2026 21:49:11 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ea27c3dd37b5ee6373dc8d74d0fea243e928d5ed12a72a4721dd95384d16d`  
		Last Modified: Thu, 12 Feb 2026 21:49:11 GMT  
		Size: 14.2 MB (14220504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01ab3f2b705b5925cfdc132d21360c37c53e1c7d6e290913e13d8e4928e634c`  
		Last Modified: Thu, 12 Feb 2026 21:49:11 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3f7196164b0a3bb00a97417dd84f9dd10d940137bc1488db370ad099ffac0a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 KB (248394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586c2388a22015aac716e614b40d6fa3f1910d80f230909d394b4f6beba50d92`

```dockerfile
```

-	Layers:
	-	`sha256:ef3cbcd400321a810654d423191fc76ef8b68b510f42619dbbd4ddbf03f3ea33`  
		Last Modified: Thu, 12 Feb 2026 21:49:11 GMT  
		Size: 227.3 KB (227271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae2f7c6f3460406bf3cc5d2c929279b9a7a1381c04d74c25f7eddaadaa0c979`  
		Last Modified: Thu, 12 Feb 2026 21:49:11 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:40b1410aeb449d0ed3d54c3c7aa45401ee11b35cefaaddb07c6e4b58197e74bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19905611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9780d86157a32ed134b3c5291c4a48acf857fc7ce6d960dac4ef92b0abe53086`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 01:02:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 05 Feb 2026 01:02:02 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:47:40 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:47:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:47:40 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:47:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:47:40 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:47:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:47:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:47:41 GMT
USER haproxy
# Thu, 12 Feb 2026 21:47:42 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:47:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1a3c9b23f916e4c28eda91c4716cbb12c72a87db35b7b5da01ab33b1261358`  
		Last Modified: Thu, 05 Feb 2026 01:03:16 GMT  
		Size: 865.8 KB (865829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918fbf427d1b030757c848f48e4b6122f1cc20612b0cdb6f69615da40bfff160`  
		Last Modified: Thu, 05 Feb 2026 01:03:15 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202646c6cf0a25d6503a8d019cdd688923474a5f1b3f16b229bec313a407504`  
		Last Modified: Thu, 12 Feb 2026 21:48:09 GMT  
		Size: 15.2 MB (15208692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1723d45685747c38a23ba99532535fa09254eef0db5f323bd58077b92c4eca1d`  
		Last Modified: Thu, 12 Feb 2026 21:48:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:736ed4aafd8b781b50c48eedfc44c14e8a433f2295172f509fd4834a40828cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6783dd9e2ca94fb6c91c8ddb423367eb08bfc9f8ad0b40f69eeffa29df937395`

```dockerfile
```

-	Layers:
	-	`sha256:b2ba3f95b89a1d16bb66811f63e2878786183ac240761571ed369b25d6341a10`  
		Last Modified: Thu, 12 Feb 2026 21:48:09 GMT  
		Size: 226.7 KB (226701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c10e4ea998f85f0977a746a2a7bf8e9860875ad9fd918148d1813aa31b2fe098`  
		Last Modified: Thu, 12 Feb 2026 21:48:09 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:41c6755c79ab65bb937ff9b854c1ba67580db8898b288762c0457483e35cbd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19997339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e215c7dc64dd1036b79f8c590aee6a242986a150edbd8c9544b9124a42131828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:30:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 06:30:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 30 Jan 2026 18:52:00 GMT
ENV HAPROXY_VERSION=3.3.2
# Fri, 30 Jan 2026 18:52:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.2.tar.gz
# Fri, 30 Jan 2026 18:52:00 GMT
ENV HAPROXY_SHA256=7295cbc26cce19434494d54d9a810be8fdf3d35014b2ed3238bb4851a63792cb
# Fri, 30 Jan 2026 18:52:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 30 Jan 2026 18:52:00 GMT
STOPSIGNAL SIGUSR1
# Fri, 30 Jan 2026 18:52:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 18:52:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jan 2026 18:52:00 GMT
USER haproxy
# Fri, 30 Jan 2026 18:52:00 GMT
WORKDIR /var/lib/haproxy
# Fri, 30 Jan 2026 18:52:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c9470919a79f39f2a2a1db9bf476647c20b35b6e97f36111db731eafdd6c58`  
		Last Modified: Wed, 28 Jan 2026 06:46:56 GMT  
		Size: 849.9 KB (849900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495b0565d23aaed2a0be6162e94f23c2de4ca298bc65512773f4fba68e98bf5d`  
		Last Modified: Wed, 28 Jan 2026 06:46:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44757abe55700b33b854c00a117a86fbf469d2e84e9fea141cd56720091c827d`  
		Last Modified: Fri, 30 Jan 2026 18:52:51 GMT  
		Size: 15.6 MB (15560708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7a7184917ae1ecca21c05ba2d2f10e9baaa5eec040816c8da4280e76f4bd22`  
		Last Modified: Fri, 30 Jan 2026 18:52:49 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:6b7f5fd4ef0d92f0526c2436916e583f3b8323977a18989feb6a436a1c983ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df16ac7884bb9c1e08013464dc1bfef00b2db490327e397faf16f83ad3383149`

```dockerfile
```

-	Layers:
	-	`sha256:178adf4e93e565824766b733c672f015f367e3892a8a7b9c7409c4b1adf3bc29`  
		Last Modified: Fri, 30 Jan 2026 18:52:49 GMT  
		Size: 226.7 KB (226697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684b9f7d789d478c27312556687f1fbc83e735f07d415c3f8ceb99af0dfcf504`  
		Last Modified: Fri, 30 Jan 2026 18:52:48 GMT  
		Size: 21.2 KB (21228 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:4b9f1596d450bb3dfcb6d86f05f8699eb147ebed59448dc261baf9159a925ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19444124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fd3a3ceadf2e233170b14d723270289b74271ffe6cbecd402800d5c7379224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 22:56:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 04 Feb 2026 22:56:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Feb 2026 21:51:29 GMT
ENV HAPROXY_VERSION=3.3.3
# Thu, 12 Feb 2026 21:51:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.3.tar.gz
# Thu, 12 Feb 2026 21:51:29 GMT
ENV HAPROXY_SHA256=0ea2d0e157cdd2aff3d600c2365dadf50e6a28c41d3e52dcced53ce10a66e532
# Thu, 12 Feb 2026 21:51:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 12 Feb 2026 21:51:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Feb 2026 21:51:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:51:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:51:29 GMT
USER haproxy
# Thu, 12 Feb 2026 21:51:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Feb 2026 21:51:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fec38153fb047f5b60e2cc698420dd7dab5ae24b9db6a21457f38690fb9126`  
		Last Modified: Wed, 04 Feb 2026 22:58:09 GMT  
		Size: 891.5 KB (891544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87dde08c25f7b3657c22bf40380e576cc6e4eab5d2b1419705369214a24340d`  
		Last Modified: Wed, 04 Feb 2026 22:58:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06127c9e00fe6a70eb9524b2caabb4680a6e5fc548c7e1c2a034e6dca025e4fa`  
		Last Modified: Thu, 12 Feb 2026 21:51:41 GMT  
		Size: 14.8 MB (14825810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7ef6e39c5b99c9302c4a0579afe0847e8f89ce2383eef28895f47074c5057`  
		Last Modified: Thu, 12 Feb 2026 21:51:40 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ebbf5c7d5dc889b3837f4a15a316bd45716a4854d8c66cd09eb4f1c0b33bdb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141c532e1afdcfa8658c4e05a2f862b06b7b6d69697a3782402075c6d1a8388d`

```dockerfile
```

-	Layers:
	-	`sha256:df2b4a16d05ffa10d25864d98cc42caa1e0bd49f9a778d3f46bf79c2c7f03419`  
		Last Modified: Thu, 12 Feb 2026 21:51:40 GMT  
		Size: 226.7 KB (226655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8837b423e3f1f0ec95dc587075c8c4e494a9e1ba8b9c13bd91b74be341fdc462`  
		Last Modified: Thu, 12 Feb 2026 21:51:40 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json
