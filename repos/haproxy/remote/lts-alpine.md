## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:00ce71e6edda9516f06c42622252c6932d4b254f305d866d3d1fe4a11b474098
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

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:9838d400c0b6a270f3e0a23893b7d557eba30fad29ca9909e868249770ee8360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17735963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ce126494f3ceb3ec3af3690c41c9af27180ae2db833ba2d5d27c0a3edb01c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ebcecb52f0506b13ed82fe49dc107c18dc647c19e57032eceb4b0b1341e54f`  
		Last Modified: Fri, 03 Oct 2025 18:31:21 GMT  
		Size: 291.2 KB (291204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bedaf7f2affe8e29b429d7b7f261f25f925a2e280c5c4623db21065a7604ff`  
		Last Modified: Fri, 03 Oct 2025 18:31:21 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf6015cbb4e862441a78ee2fcd04081023bf5834f01c09ec2d7aa63d852415b`  
		Last Modified: Fri, 03 Oct 2025 18:31:22 GMT  
		Size: 13.6 MB (13643632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0af98c4e4fa3a8f0f4f3188eb3c4ee1fc674dad29a820390a1b82754a1e73`  
		Last Modified: Fri, 03 Oct 2025 18:31:21 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:4d7947108d8142d0b03248fcc4047dc49f730032fb91118e2ec4e4da663502f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 KB (209551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90241572e29708077b5271c13374d44df15fe2d86d83feb4581bd7dc37357fe5`

```dockerfile
```

-	Layers:
	-	`sha256:71d2637e75d1a6be219ab50fdf7a13a8adfc541aeddfc9498231618d9d71b720`  
		Last Modified: Fri, 03 Oct 2025 22:01:42 GMT  
		Size: 188.7 KB (188664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833ef6b5b57c2e0cdcad0baf8ead27da24f2f46dad4674ea67b1e773992363a2`  
		Last Modified: Fri, 03 Oct 2025 22:01:42 GMT  
		Size: 20.9 KB (20887 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:5955e19a342926a65d9b341322c263d884fbff7621bfa4b0a27be7b257c402da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17169552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f8051de4c93ce5acbd6bfdc870203b24573fd11366004b364cccb53d1fb349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ee5b025ab8ce3105fb6bf3b820f36019e707573e7ead717e7a2a7cd767c6f`  
		Last Modified: Fri, 03 Oct 2025 18:31:04 GMT  
		Size: 292.4 KB (292397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239d2da0ae37c9c11144f6f7508f252c40ae86222f7b21b872860c1a18ddf59`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc415f4043c0a0fc66f1fc29491f33dd33324206bc4b517d68f3b2de6e41eb20`  
		Last Modified: Fri, 03 Oct 2025 18:31:13 GMT  
		Size: 13.4 MB (13374806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bc034cff91163a2ac83c6935669a61a5753d3a8d45f5ad2bf7e36233ed2e5b`  
		Last Modified: Fri, 03 Oct 2025 18:31:12 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:8ac86ca38b4bb865bf6b9f958023a30d34747f76fee5ad4272ad9d1831da6e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237f0a793ba89f8d30f9d8374968433f2f7eff1647758c46a51a62719cba6ca3`

```dockerfile
```

-	Layers:
	-	`sha256:6b5c3d45b3fe2bda27526ae6b75259daacd9746f0864c94d62352c19f157c754`  
		Last Modified: Fri, 03 Oct 2025 22:01:46 GMT  
		Size: 20.8 KB (20810 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:063d7adcc8ee5cdd688c0bd758ba574df87fa52715dc2dc76f7c68287dea4968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16555481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee90a50182c5c29bb7300f8abe65ac33c284a0360bfaf311e7610e74a3a469`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c0fd7221a38f1a02a1608f1a460e5ad5c2acebbfdcf99c2f802763b664890`  
		Last Modified: Fri, 03 Oct 2025 18:33:17 GMT  
		Size: 291.3 KB (291253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b311e36883339c6fe20534b1dcc1ba357a6e7f80ce0318246df0a5318e04dc`  
		Last Modified: Fri, 03 Oct 2025 18:33:17 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd646b7322583840b53ebbd619c6ce80d148d3d101d4edfa279f30ea6ad8793`  
		Last Modified: Fri, 03 Oct 2025 18:33:19 GMT  
		Size: 13.0 MB (13043746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d61fc8f7a2d4869e8f7e9a2a8afc62caa34097bb226f79363ba27c136166ec4`  
		Last Modified: Fri, 03 Oct 2025 18:33:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:c8dcaa339d8b841e48ce76a695f55d5da7cd17fcdd31a7de5f32c92dac77b923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 KB (209757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b359de315cf020997d51f9a06ba3c3ea783456d1d0b368b76ac4f3f5dc67a35`

```dockerfile
```

-	Layers:
	-	`sha256:8287c22e1841ed105ac3d79fe25b8e25493e36c416327da2b2fa5f46e35d8bc8`  
		Last Modified: Fri, 03 Oct 2025 22:01:49 GMT  
		Size: 188.7 KB (188732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56ac1ea0692fa80f9d3e49a485686a0ffd59b60f10f7433bfef110cc071cf2b`  
		Last Modified: Fri, 03 Oct 2025 22:01:50 GMT  
		Size: 21.0 KB (21025 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ebb97ad86e4c6907db61f657807aa1efec3f38c3cdc893c3506111a48ca25866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18300170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccda1321f41c8c500d493497e61aaf9650b51c9072e3c1f88a9b69488796f1f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069fb810606918c81896bb4459c6cf7deee0543ce9bf4b644b0755c952b64bc`  
		Last Modified: Fri, 03 Oct 2025 18:32:25 GMT  
		Size: 294.2 KB (294165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acaeb0180ddf0d9633b7279f8a0562b79a85fb9dc84b38db71ffd1729825754`  
		Last Modified: Fri, 03 Oct 2025 18:32:25 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5646bf34a1a8075f3616a1563594d6fd0ebe77d117aebd3c8295d083aad6ab53`  
		Last Modified: Fri, 03 Oct 2025 18:32:26 GMT  
		Size: 13.9 MB (13873817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05282afaf82496e1028edd35544df5c347652a65eea2087e66930dcf6ffa3abf`  
		Last Modified: Fri, 03 Oct 2025 18:32:25 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:2b4cbcc89f211f418f4c418cda9b257c4fdfd9e1e63c80e4f752f74821c05bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 KB (209836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8713c1a46160c724a050721e0d47fda77b6b3b0bc7f61819004061c15538fae`

```dockerfile
```

-	Layers:
	-	`sha256:1f2cd63c4e83ba2957bda001f06455e11e92a09a5cd72fa6d9302982f316e619`  
		Last Modified: Fri, 03 Oct 2025 22:01:53 GMT  
		Size: 188.8 KB (188768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b501f7e7bc523430269e4306ce2c5c22afe4d21141eab4acf1fe99aba888ab`  
		Last Modified: Fri, 03 Oct 2025 22:01:54 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:15530fb026eaa3a16f1fbc42cb348fe4cc4166c3edde8bad91c00b7ac983181c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17084222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458c5554a6408aae2de7084b39cffaeed3b984a595aa8b58979b7d8dd6bff5d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21563efd77e29321c29f530769760a1c6566879b28aef7f6bc85b9d7927254e9`  
		Last Modified: Fri, 03 Oct 2025 18:31:05 GMT  
		Size: 291.7 KB (291675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c014be04c08bd9548a9b4acc3434a7bb4697a6c91f2f541fc325976ae922b22b`  
		Last Modified: Fri, 03 Oct 2025 18:31:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6883c5a6aae9bd67b35ed33609de8a235b7e9d95904eae1c208254355b3f645`  
		Last Modified: Fri, 03 Oct 2025 18:31:10 GMT  
		Size: 13.2 MB (13176104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27554e8260d914b098690ab13591d71401d396ab0fb20ae40209917740f2f3f9`  
		Last Modified: Fri, 03 Oct 2025 18:31:06 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:1ac91c67569f7cfb13636deb38002129da38affb13a35f31722a128965435917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 KB (209450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553f776b06bf3bf02cb3819c820b3cc46379aa8e8de6e6861328f080cce17259`

```dockerfile
```

-	Layers:
	-	`sha256:2092dde3e53824a82c4baca322dec9e3d8a6dac07d681bef4ae48825a7799124`  
		Last Modified: Fri, 03 Oct 2025 22:01:57 GMT  
		Size: 188.6 KB (188619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a2d6c85a46b4161cb31bb33c788014fc566c48257a1fb35cdbd44d64baab4a`  
		Last Modified: Fri, 03 Oct 2025 22:01:58 GMT  
		Size: 20.8 KB (20831 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1a3131b417a10f7a7c6c3bf4c25dc991e8bb3dd38c60c92c0b65b3080c4ea1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18140139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf8b4273166236c18fea7c1bac367b794edd30eab992c119e46639519875067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8732dec6cd543e401e26e214c4c77ec3dee44b995d51b60cbc3b80fc6b5b7b5`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 294.6 KB (294629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41efe5ccdbe71c63281e775f25396cf39efc8ad7483b30056ab71e3744bc55`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b302c8f3f70fd6d7d607cbe458ef0d36aeb3acad1d39820d40de5924b3fc2b13`  
		Last Modified: Fri, 03 Oct 2025 18:34:00 GMT  
		Size: 14.1 MB (14116958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f7d14897b557f69e5b35619ad4d2c6fb4e586a5dbd20d5eee31c2c4e68bb14`  
		Last Modified: Fri, 03 Oct 2025 18:34:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:cafa3d4c3f65c173882c32a2db21418292f54dce921f481feefb773461a22e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 KB (207730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492a8cd7afa9e8bd6c8d9a4cf4efa8b4241c3f8ecca1509fa546cfe650f61574`

```dockerfile
```

-	Layers:
	-	`sha256:7e75bde25d027e4b0a457b442c6202dd0b8f914528c7e1ab2fb3ceb5b9edb5d6`  
		Last Modified: Fri, 03 Oct 2025 22:02:01 GMT  
		Size: 186.8 KB (186771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b002b17fec91a0917670a6080481fedd3804b5a690957ab2c52d166fbfd95f`  
		Last Modified: Fri, 03 Oct 2025 22:02:02 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:37a96cfa28accc8c627cb26e57ae3d88ef96eb7d36852c2b4b25819d8a3189a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16783080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4526169ddd00a3ddbd9e0910f7991b0eac0a169b4e193b916591f3dbd33b2fe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c1b0b12556f919041bab74993c8b60266f3f41ca4cb1eedc7f2a1316ea78c5`  
		Last Modified: Tue, 23 Sep 2025 18:43:52 GMT  
		Size: 282.8 KB (282799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9672f94f2d57a192202d473cf3e8849e54f92fa36d2fd0657c8a26ca94a75f`  
		Last Modified: Tue, 23 Sep 2025 18:43:52 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5319cda9f00646741902afe932beb652d29ae7bc7bd2cc3db2c759ac622983d2`  
		Last Modified: Tue, 23 Sep 2025 18:43:53 GMT  
		Size: 13.0 MB (12986033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa4ff3f0c048141c1f6bb1af7cf830912872a56627fe5d2f7815de8bff4b617`  
		Last Modified: Tue, 23 Sep 2025 18:43:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:373311f6709d4f7e103d0923a7872b17a86f6e376b1da34ccfb1f122e8003f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 KB (204030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63712120a15eca0958de203ec0325f50bebee7904a46bc8aa5610bc7e81c9cd5`

```dockerfile
```

-	Layers:
	-	`sha256:645c6d6d51cfdd7aac792e828e35bba8b16cf14cb3515d483c05000d58c90945`  
		Last Modified: Tue, 23 Sep 2025 21:56:53 GMT  
		Size: 183.1 KB (183071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d746345c75ed7c23cba938621cf7a2a6edd47deb59d02ade714f93b57a429ada`  
		Last Modified: Tue, 23 Sep 2025 21:56:54 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:d8d64c68b922825f36cb7109f648c9ffa114daf3070155852e0f3fab736606a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17714650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42521b17baf5af81c01c9a553316b921ba22ed154e44ab4abbd26dc7805fcfdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbb9ed5d056774b0f6fdde4aa100dbf4765f9ac187950a0e9742d065c307fb3`  
		Last Modified: Fri, 03 Oct 2025 18:30:09 GMT  
		Size: 292.2 KB (292191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0feeaf75f6a418852418391369c7b138f0a9223b2a4a67c5b29f6c1ac5b589b`  
		Last Modified: Fri, 03 Oct 2025 18:30:10 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63793f4ae120e7fe8ad35891af07c1458b24d3b1d95166bfab4abf0e0e5dc2cf`  
		Last Modified: Fri, 03 Oct 2025 18:33:02 GMT  
		Size: 13.8 MB (13776046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b751f9f533dc74ba15d2b4d998272b066119d01865b43cee3e1376c359bf77`  
		Last Modified: Fri, 03 Oct 2025 18:33:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ab9c8971e73699ea6518511e465cb1d93e38d4736244c7f9ff148f76d72f67a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 KB (207599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb58833a36696f7939ef9c5dc51a3b15907f03d0c4e24fd464db4978a81a80d6`

```dockerfile
```

-	Layers:
	-	`sha256:85c184e52baa3218501345da7b0fbdabf97e8e5942326fbb8da81bbc9fc1dad5`  
		Last Modified: Fri, 03 Oct 2025 22:02:08 GMT  
		Size: 186.7 KB (186713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e467214e85cd8f1e4bc9003956b195fb877b3f596acf9701fdc59bd42b1d832`  
		Last Modified: Fri, 03 Oct 2025 22:02:08 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
