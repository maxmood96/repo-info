## `haproxy:alpine3.23`

```console
$ docker pull haproxy@sha256:debe69a8edcea8e8f6e240c346ba19a6fa0bd86156285a36aa888344a8604f5e
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
$ docker pull haproxy@sha256:cb0f60a6aaf129b91584183555574a8109c8b67787b48c4cd09598acb5656f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19185666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404f01ff4cf3e0979ac3ea81e0778d88b631a0b8201a046de95c4f9f06dc3f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:33:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 09 Mar 2026 18:33:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:34:07 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 18:34:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 18:34:07 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 18:34:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:34:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:34:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:34:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:07 GMT
USER haproxy
# Mon, 09 Mar 2026 18:34:07 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:34:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a92bf344fff6f95a8eb9b9cfb1d1113f9cc556c23dcd63f716e99b65398614`  
		Last Modified: Mon, 09 Mar 2026 18:34:13 GMT  
		Size: 829.6 KB (829635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ef5c6af0eafdf395cba48716c40cd25f57a1c1174fbc84be728b4dee8d376d`  
		Last Modified: Mon, 09 Mar 2026 18:34:13 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95241bd49edf9c294239497f2bbbcc33ad29d115d43558d797090ae377490a2b`  
		Last Modified: Mon, 09 Mar 2026 18:34:14 GMT  
		Size: 14.5 MB (14492771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1613639b32ff5b18d506626802e7bfe13db1e48e830c862d4ced3a5e2caf5b93`  
		Last Modified: Mon, 09 Mar 2026 18:34:13 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:adeff8b7efa7baa055774eeb371c9a758804cf3c4c42f345ac3e51c6bd00753a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 KB (248475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e26797e1411535d340522ea5d239a294e673e54617fc8b017aa73d1a65b310`

```dockerfile
```

-	Layers:
	-	`sha256:4358076ba73916d19c5ef0992f404adb74f233b67a76d7c70efcc943dfa2130d`  
		Last Modified: Mon, 09 Mar 2026 18:34:13 GMT  
		Size: 227.3 KB (227306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008e10d1214132a2e5a135827026f3d1ec97a65ab346c5ce82540e681f057e55`  
		Last Modified: Mon, 09 Mar 2026 18:34:13 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:934eb0005ea24680348a79dc736c07d1312386454863250683f546e353e78abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19103883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91f9ebdf5717ded3a5935ccdcf2f665748daeb99cb2bb36b3b80750006492b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:45:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 09 Mar 2026 18:45:49 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:46:34 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 18:46:34 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 18:46:34 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 18:46:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:46:34 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:46:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:46:34 GMT
USER haproxy
# Mon, 09 Mar 2026 18:46:34 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:46:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ee7fa549f8bb345c57784160e0608a903f66218a8d6139053f190816f78d9`  
		Last Modified: Mon, 09 Mar 2026 18:46:39 GMT  
		Size: 821.9 KB (821850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addad2aac651fc07a2f90d3e6f9a786643eb6bae3890c83fafb3a98bcb8341bd`  
		Last Modified: Mon, 09 Mar 2026 18:46:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6868786e32c3f41ca72af605de62cbf8369289891e792d5fdb7576a981eb7e`  
		Last Modified: Mon, 09 Mar 2026 18:46:40 GMT  
		Size: 14.7 MB (14710777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dd288fed3361152d9c2f2801adb4d45a8753bd1ea2f85d4b4236919c47bce8`  
		Last Modified: Mon, 09 Mar 2026 18:46:39 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:ea348bf8b2350e31cef33cb888cb63aa5b7b7b969f762bd8359878adef77e10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e430d18f2e70937af69d9ef40660546cd4e9aaad82e449340d5ae75f1cf3e5`

```dockerfile
```

-	Layers:
	-	`sha256:cc630de8e93e8a69b29d0f678f620e676d8a667803c8c1b4976900865eb69d46`  
		Last Modified: Mon, 09 Mar 2026 18:46:39 GMT  
		Size: 21.1 KB (21076 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:de7da62528403e721b002b18f7e0e18734e0644aa8fc3617d40fd7c7984222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18613081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a82be0f81fb118aeaedf51697fd3b2a879ab43a14a080d02cf00dc31f0ea2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:50:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 09 Mar 2026 18:50:49 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:51:36 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 18:51:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 18:51:36 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 18:51:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:51:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:51:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:51:36 GMT
USER haproxy
# Mon, 09 Mar 2026 18:51:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:51:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91abce714c98b2900aac47d0e4a473d5e78a2d30c514555dc0d62aeec51703f2`  
		Last Modified: Mon, 09 Mar 2026 18:51:42 GMT  
		Size: 777.7 KB (777712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbf1976b712c9fab950bba7d6ab7b19e30da1babb4684ce1d1c3ed207b2e127`  
		Last Modified: Mon, 09 Mar 2026 18:51:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8e6199bdb6f08390f4a124200715b57cfd2c2cb2bcea37238494723df62f1`  
		Last Modified: Mon, 09 Mar 2026 18:51:42 GMT  
		Size: 14.6 MB (14552209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac249141168077c34562cb88ec852d2defac684cfaee8e1df5316c1a7ef905c`  
		Last Modified: Mon, 09 Mar 2026 18:51:42 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:8238df9a73fe367ec73b63e84c13af23535ed02ba7c3c671aa584e0a0004bb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89398393c5f697fce15018f71c452cb2b28570a912fb4fc5ab6731d79687a9b`

```dockerfile
```

-	Layers:
	-	`sha256:be68588254d164f4b6876ed5b5f28684535e173208ae24b50388e0ae3c8ea936`  
		Last Modified: Mon, 09 Mar 2026 18:51:42 GMT  
		Size: 226.7 KB (226708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9dee4011f55523ea6301e582bf96d7643e70c002c960299cd6de5ac24ab8d1`  
		Last Modified: Mon, 09 Mar 2026 18:51:42 GMT  
		Size: 21.3 KB (21291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:5293bf8c482cf7f4533e46375a78c1733934ebc297b50953e723e68f44a71e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19288712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4c137345ecf27eb6b89f2dbc2aa4784a012fa8f037404991f74944626594dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 09 Mar 2026 18:34:52 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:35:34 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 18:35:34 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 18:35:34 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 18:35:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:35:34 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:35:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:35:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:35:34 GMT
USER haproxy
# Mon, 09 Mar 2026 18:35:34 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:35:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39eb7b6f98c9871f57360809e2a4562801e07c39e8b8d1d2c9816b6c7b1462e`  
		Last Modified: Mon, 09 Mar 2026 18:35:40 GMT  
		Size: 842.4 KB (842381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267299cbde311cc866d29070ffb800b0b096d2a7e5c97890f86dbb155159eb8`  
		Last Modified: Mon, 09 Mar 2026 18:35:40 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0d8851a7594675906b356e989c2e02fcb35e29ca3d915c2d13f025b4e5166e`  
		Last Modified: Mon, 09 Mar 2026 18:35:41 GMT  
		Size: 14.2 MB (14247803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad1c6a591cd3691317fb03f6d76758f3b141fbe0b41914fc07640ae4d82cdd`  
		Last Modified: Mon, 09 Mar 2026 18:35:40 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:915413ccf4cb3b545d80db0cd0843b5ccbbcb495649977daa62f8e2aa0800395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 KB (248063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96911eff3eeeceeaa722fb0635837e4ba0838e7ad5563b06ac0c2fb210353b9b`

```dockerfile
```

-	Layers:
	-	`sha256:030bcdfeb5cc4787bea263cb9378b287bd43c02b8992bdb80332306f7679d468`  
		Last Modified: Mon, 09 Mar 2026 18:35:40 GMT  
		Size: 226.7 KB (226736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ab37f31ce9169483aa6a162dc1ad9432d696ebcbacc76d6cf7b826f033c8f1`  
		Last Modified: Mon, 09 Mar 2026 18:35:40 GMT  
		Size: 21.3 KB (21327 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; 386

```console
$ docker pull haproxy@sha256:dafcb6c1eb87b9fd188272e4c49deaad96e1d9d9d1d6d9e6f5228d7fb37aa837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18806227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3222b5dbee37a0dbf7dda2e33603e695e33f0e8f89dccb4b6b8e3d3c42ec77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:20:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 09 Mar 2026 18:20:13 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:21:05 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 18:21:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 18:21:05 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 18:21:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:21:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:21:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:21:05 GMT
USER haproxy
# Mon, 09 Mar 2026 18:21:05 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:21:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a324badfa92d3e18331a3119e18c1bdc4c316a585ff47da5dd7dd576b25986`  
		Last Modified: Mon, 09 Mar 2026 18:21:12 GMT  
		Size: 835.9 KB (835929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75571d520d8b43eb17f7cbc025934a1ae02adc6dce6e8aeb10ce8ae3598e503`  
		Last Modified: Mon, 09 Mar 2026 18:21:12 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb7c7803f4c3afebde56115696a46a2c21a948e500e8261c18e8e712293f461`  
		Last Modified: Mon, 09 Mar 2026 18:21:12 GMT  
		Size: 14.3 MB (14281865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e403285a59dab43339b39ec8cc008e45f9fcf7fe8cc88a6611628c823debad`  
		Last Modified: Mon, 09 Mar 2026 18:21:12 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:3f6d426606be194a935384b96f56b596dd747a52889b68912fc027dbf3f9eb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 KB (248394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0329a433dad595f376d209dd81d1e86c655f2a07799077bb337d6fa565bb39`

```dockerfile
```

-	Layers:
	-	`sha256:d5233ae4133b69cd6061494187cebb6bc2939758858b8e610602fd0401af5a43`  
		Last Modified: Mon, 09 Mar 2026 18:21:12 GMT  
		Size: 227.3 KB (227271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d7de50c81e9f72f46cb7d8fd8a3cdb8c03d83ccd6c3a6376455cf68aa354ea`  
		Last Modified: Mon, 09 Mar 2026 18:21:12 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; ppc64le

```console
$ docker pull haproxy@sha256:171f9fc0091f898720e42501375387c8c8007d86435b5f115108d5465e6e534b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19980626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd213698afa827e85fb28e6109e872549203cdc064a16f0ccec063f2778b3ed9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:51:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 05 Mar 2026 17:51:38 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 20:14:38 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 20:14:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 20:14:38 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 20:14:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 20:14:38 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 20:14:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 20:14:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:14:42 GMT
USER haproxy
# Mon, 09 Mar 2026 20:14:47 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 20:14:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d053544bf9bf17c9af94492ed0367531ac5fdac288d34d557c160d34a64d63`  
		Last Modified: Thu, 05 Mar 2026 17:52:42 GMT  
		Size: 865.8 KB (865834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bda81e5fca82f954a3c08f03d46a5a3950ef62f631570c14eb6929402b112`  
		Last Modified: Thu, 05 Mar 2026 17:52:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee0245cc3e83a11c14e4892831db7f29922e473808cdb0c33f8e9938f0f9de`  
		Last Modified: Mon, 09 Mar 2026 20:15:05 GMT  
		Size: 15.3 MB (15283701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a4125e837d96897c46bded5b22c08b64a94445e45dabacd42808cd3c918e4e`  
		Last Modified: Mon, 09 Mar 2026 20:15:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:2cba5c3a886ac2fc67d57ef3a18f44f6e7c66094274ad060081ad630f716cb77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d47cc3e3608df486e71d5e80b61a14ed7d97b7f575b467d5c6483b6f1f3357`

```dockerfile
```

-	Layers:
	-	`sha256:8c1520d23e31085fc5a8ff178933e82ddb9b1b62f7701b5a7af3a6165e809d4a`  
		Last Modified: Mon, 09 Mar 2026 20:15:04 GMT  
		Size: 226.7 KB (226701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7768d686b5fbc23a3e187dd3090d0cc83598ceae213f586e127d51a05a7d8f2`  
		Last Modified: Mon, 09 Mar 2026 20:15:04 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; riscv64

```console
$ docker pull haproxy@sha256:9a025358082e97fd8c83ce7aaa55cbf74656cd2eb0097ae2220162cb4b24d7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20076477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ba211aa3c0a5c1466b9bdc1cc8d5d9f8d4360596e850db712924adcb741c2`
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
# Tue, 10 Mar 2026 02:51:00 GMT
ENV HAPROXY_VERSION=3.3.5
# Tue, 10 Mar 2026 02:51:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Tue, 10 Mar 2026 02:51:00 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Tue, 10 Mar 2026 02:51:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 10 Mar 2026 02:51:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 10 Mar 2026 02:51:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 02:51:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 02:51:00 GMT
USER haproxy
# Tue, 10 Mar 2026 02:51:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 10 Mar 2026 02:51:01 GMT
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
	-	`sha256:37b120c371bba8e867134d2f262e16c794e6066a3db9bcb5cab2a3edeba10309`  
		Last Modified: Tue, 10 Mar 2026 02:51:51 GMT  
		Size: 15.6 MB (15639846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21f0f9be3ae2d40a4298c0b071e7bbd90f86da85fca2fab77ced9a401f275b7`  
		Last Modified: Tue, 10 Mar 2026 02:51:49 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:236e0ccb2e209d6bc55617a665666db67c9ce18f45477ca9d5bc98da4323da0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013bd6382f0d106286413dfb5af3895f764d9d8e73de9be2f48077ed6cd4f52c`

```dockerfile
```

-	Layers:
	-	`sha256:34ab73d76fcc4df28dfa5bc42785f3837e712c26255d7b56f93a553ca118550f`  
		Last Modified: Tue, 10 Mar 2026 02:51:49 GMT  
		Size: 226.7 KB (226697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c78cd47b8541d3443a8238f5768bac5f00322b02ed89ac1a2eba9ed7c8e5ec4`  
		Last Modified: Tue, 10 Mar 2026 02:51:49 GMT  
		Size: 21.2 KB (21228 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; s390x

```console
$ docker pull haproxy@sha256:85fe038f6f891ccf453eea7399aabdae40245106382916ab782998d73d7b8357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19509517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0fee2392a670436682b50d76e7c680412c4421b7ead7ec6328bef21ed9e3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:47:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 05 Mar 2026 17:47:19 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:58:32 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 09 Mar 2026 18:58:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 09 Mar 2026 18:58:32 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 09 Mar 2026 18:58:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:58:32 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:58:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:58:32 GMT
USER haproxy
# Mon, 09 Mar 2026 18:58:33 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:58:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f936e6d7cfde53d073d2c73ea3a8e25e648ed28692ec2a4adc7ed6c81635eb`  
		Last Modified: Thu, 05 Mar 2026 17:48:33 GMT  
		Size: 891.5 KB (891549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b609d71cf78d10250e52bcae282cdd2d7116b6930443a6db039e3cc869055ca7`  
		Last Modified: Thu, 05 Mar 2026 17:48:33 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ec13bbd338ead739ffa9bc85c637f6a40098cf9f2512b5ee7fc054a9d1047f`  
		Last Modified: Mon, 09 Mar 2026 18:58:43 GMT  
		Size: 14.9 MB (14891197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415b3228c8a76b25f4a65acab0181ce2a41a55efd0df161b538a27aa6e9dc94b`  
		Last Modified: Mon, 09 Mar 2026 18:58:43 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:8012dbd1d2c08b2a8d7b1e8035ce58f15a1f86a8b211a7c236ea57dbcaebe685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fffa1199a9cfa3d0201774f1357599e438661140d981d9092b28c3e9be64b2`

```dockerfile
```

-	Layers:
	-	`sha256:e0f1deea485cd6c63befa333729d65b3f71bda073da10c910247773478ea7283`  
		Last Modified: Mon, 09 Mar 2026 18:58:43 GMT  
		Size: 226.7 KB (226655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f08ad9df299c543a24b1fe6ae28fe1c4557800ecf8293dfb0f23f324764913`  
		Last Modified: Mon, 09 Mar 2026 18:58:43 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json
