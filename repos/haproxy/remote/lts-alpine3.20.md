## `haproxy:lts-alpine3.20`

```console
$ docker pull haproxy@sha256:d371c2a06a9f021509d6c44f9cba6b80d9c647d04566ecd55605bd70c01bd99c
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

### `haproxy:lts-alpine3.20` - linux; amd64

```console
$ docker pull haproxy@sha256:23d694d1ecf7da0882280bc42c588da2b107e96407775fc9b8938757d60f99b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15641687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d1cfe121f3335142ede77a3bef7a38735d14e5906b3e3c70ee81ce00ccdd07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa720fe293b2c5c01e374d306788fb9bd2bfc0f22780c2cce01d6fc81cfff8be`  
		Last Modified: Tue, 12 Nov 2024 02:19:36 GMT  
		Size: 290.9 KB (290894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0604a1c100a12ad4da9540b38a761afc6e16dd587d03268d4d10e397c8320fd`  
		Last Modified: Tue, 12 Nov 2024 02:19:36 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c83b115d4820d1a5d915b27d96d93df4a96153ce4d1681ed7f0585fbbb31ff`  
		Last Modified: Tue, 12 Nov 2024 02:19:36 GMT  
		Size: 11.7 MB (11725429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287d783e72b1ea4bf43d7b4634e084d0e794fbf4d627df6582b73b9365ffffb`  
		Last Modified: Tue, 12 Nov 2024 02:19:36 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:2317cfd81994703883b72d5cf52a6ff95125a9a095ffabaf9b9d0ade4f3a07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49508ed3d9104d507f04d03e325bb8d9e57563f3e23b67631627c5379f842f24`

```dockerfile
```

-	Layers:
	-	`sha256:954acf06ce829292ae48300da4a4f9eb3680b495acbfd22d746a1c53c4d31bff`  
		Last Modified: Tue, 12 Nov 2024 02:19:36 GMT  
		Size: 180.2 KB (180218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb96c566eb12e5649c8b78a43673ebba7156c2af9d44a2dda589b8fcd9ef4d43`  
		Last Modified: Tue, 12 Nov 2024 02:19:36 GMT  
		Size: 21.1 KB (21073 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:0fad6949eb0a8f5b84c19725982ca2889154d9e03e9b943dc0628f46001a58e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15077298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766781c33546645b3c3d3edde904c818cc1d5b5c8a88ffa3d74160da2d4ef72a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b506ff9dcaba1b8959509e2dd40ebb5fff02226039b86e10ca1fa29368dec3`  
		Last Modified: Tue, 12 Nov 2024 02:35:17 GMT  
		Size: 291.8 KB (291776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b4c3bd7d6d27b793be61ad84883e470f72e92eaa7a51c86df9962ad290b28a`  
		Last Modified: Tue, 12 Nov 2024 02:35:16 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a5042e44aede844c002adfb5da86b6fa549e85f570e456eb337e6d3ae3ad95`  
		Last Modified: Tue, 12 Nov 2024 02:36:27 GMT  
		Size: 11.4 MB (11417473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c30c97538f8b4457d814a244f1635e3e9cdc3b8362c5eb10dee02242973c195`  
		Last Modified: Tue, 12 Nov 2024 02:36:27 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:670f4bed906f6081e52c81e2f48e6445697e47893acb51a7129c412dd379a0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d650e755967691446ee7586c25bba37dc66e7554070a5c69e9bfcc1890ab030c`

```dockerfile
```

-	Layers:
	-	`sha256:db7871e8235ef1ed89e096b3d742e0226b09c0994e973317f623f5cefb3dccae`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 21.0 KB (20992 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6265ad2525fbedf83b672e33c0ea92752e3ef4cdb52d595e6fafb3344096f6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14502569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d501342e89460748f42396df56c1c10023c55eb6c98868142fccac5bb80735da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d19af6260668ec5acebf06ca1010e7c7f5c1d62a13cc5b460c3cf3e29d8a5c`  
		Last Modified: Tue, 12 Nov 2024 02:25:39 GMT  
		Size: 291.0 KB (290959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbfe72087166183a14beb591e9018b8725bfe385e9f581cabb3ac98f8584c8b`  
		Last Modified: Tue, 12 Nov 2024 02:25:39 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a26e2daa3b76448ab36bb3113ab729c7f85cf23a7294a39617deb6ec09bbd7`  
		Last Modified: Tue, 12 Nov 2024 02:27:33 GMT  
		Size: 11.1 MB (11114668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e46373e2baa63dab42d0f80120aacfa6ac977eb249888e5f22de4ce6a85be9`  
		Last Modified: Tue, 12 Nov 2024 02:27:32 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:83aa7c5e12c2281d4321e8ca94496b4be66f2bd318579b67d21da8178c6bdf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 KB (201494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc158a6c71928f904e84a217ae060fd6763c0e9e51bc0d909d4de733a23348af`

```dockerfile
```

-	Layers:
	-	`sha256:af40f6d3c9a3b04d1ade5556e1d2bf3f4e8dc901a698dfc76c1c3d873daf91e6`  
		Last Modified: Tue, 12 Nov 2024 02:27:33 GMT  
		Size: 180.3 KB (180286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5a0651290d69ddf08bab1fecd11c965710bcd316e133d7d87d82d9530c4fdc`  
		Last Modified: Tue, 12 Nov 2024 02:27:32 GMT  
		Size: 21.2 KB (21208 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:a9b67c896495a6fdc7810e3e845e96b80c6e52d3474fb97178df784be6d675d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16515883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f25944ac12216f4d9f87050bfda0ebd3a4ea1ccad70da3615fbe0eaaeee40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43792958bab5d808836747d6b57854a03e2a1cbf7d69ea5e0e3da9df6a08aee8`  
		Last Modified: Tue, 12 Nov 2024 02:43:20 GMT  
		Size: 293.5 KB (293528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33badf9489724f855bed4273d73530e1d037eb8127a97af09f586d134338a8`  
		Last Modified: Tue, 12 Nov 2024 02:43:20 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a3b9718f5ed04d4f487d776bebe4759082518c8e64c8b1be1859a6e27843dd`  
		Last Modified: Tue, 12 Nov 2024 02:44:56 GMT  
		Size: 12.1 MB (12133171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc1e1abafcee6c83d84be75286d1d6afca50524c3d0724c9300538352af8cff`  
		Last Modified: Tue, 12 Nov 2024 02:44:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:fdb69639674e0e98a0a0b819f32179401d899c6f7ee1f1d2bb3aeaf20e34edf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 KB (201577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593a3d7088a7bb3ba3b0184c9ac3fdb995f802ed869c82912d52650abe69ad45`

```dockerfile
```

-	Layers:
	-	`sha256:0a85afbe7d4a380391a4fe770abf6cb916b8ae96e766bb0d3925c910124bdd36`  
		Last Modified: Tue, 12 Nov 2024 02:44:56 GMT  
		Size: 180.3 KB (180322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4474bca7989c561b3b2e8babc090f5713b303c719ba1a4801ae313b806b9d5`  
		Last Modified: Tue, 12 Nov 2024 02:44:55 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; 386

```console
$ docker pull haproxy@sha256:fdff8b00b5a92eb48e4386f3f559a3ec4e5bce06af6cdb3394367ca6c20d0175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15103139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eece9240d289097ad5553138db988f31aed9e60293fd6b76a7599e1c02baad1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8e0a8be5c4d1f5276897f2c929cfe8d56d6a0b0591d07e2c0bb2b4b24207db`  
		Last Modified: Tue, 12 Nov 2024 02:24:35 GMT  
		Size: 291.4 KB (291366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a025143bea91e71d34f93ab45afe459d52ed0dd3f56d8c04a808e30637ff80`  
		Last Modified: Tue, 12 Nov 2024 02:24:35 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f61e917797eca357318585ba4c7f9ba8cd72f51d689b5d380c9a89ce41450cd`  
		Last Modified: Tue, 12 Nov 2024 02:24:35 GMT  
		Size: 11.3 MB (11341097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819e71f3e5f9338b5738613deba52847d89a839345685a94ec2796873684ed4c`  
		Last Modified: Tue, 12 Nov 2024 02:24:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:b398071cd8c9799f0a3b1ce69eb8556c27ea3dcf65f84099d08f5dd24f606a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 KB (201191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a412836d6f7b506b43d6cdeffaa4b2f5e702ce7ab306b9a71e6b7b691c1046`

```dockerfile
```

-	Layers:
	-	`sha256:75c49c1642c50236d2a8178782891e644fc521d9a7a8298cdd478a88a8a99163`  
		Last Modified: Tue, 12 Nov 2024 02:24:35 GMT  
		Size: 180.2 KB (180173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f4f8df08fc3b48f964d4f5f6418df5b6b806ca8fa99bcda8a652ae2298a09d`  
		Last Modified: Tue, 12 Nov 2024 02:24:35 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0159f69e232d6816a191b857c5b3fdad13ad05b9a0845c9e3bde765824460d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15972837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49af8ac8505512d0ee81987d920599b6ec6d514eed818ed072151942f3dab57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbcc045f7f01df4c2e1e0980a209a25d67330baf9e33fe45b9da30811ab159`  
		Last Modified: Tue, 12 Nov 2024 02:32:01 GMT  
		Size: 294.0 KB (294035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107c28de93bea1bfdd32e2ee4da231215add7dcea4a44c3e02423e041f4e2aeb`  
		Last Modified: Tue, 12 Nov 2024 02:32:01 GMT  
		Size: 977.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07baa52cfc5e8eee10dce5db0d43b0a636be821e974741d69dd560092108373`  
		Last Modified: Tue, 12 Nov 2024 02:34:21 GMT  
		Size: 12.1 MB (12104889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fc0d8d7a18cddd8d3963979bbabcf47c3bf6944cacde1aad5d7308819277da`  
		Last Modified: Tue, 12 Nov 2024 02:34:21 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:bc0492c668ff80b699b71c97af31fa5eeae7d3872aa3188e964de0022f7c1232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 KB (199467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e9e8c8bfaf1b69b6a1b0f1ee63ed92774c5539612a1fd89e6e0f12bd587253`

```dockerfile
```

-	Layers:
	-	`sha256:5103a248d6b90f4c8fa1e49b59dbceb82683e3112adf5bbccc95f274c0f9d298`  
		Last Modified: Tue, 12 Nov 2024 02:34:21 GMT  
		Size: 178.3 KB (178322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779689bc9a96d093ee0b8e7cfcbb1dfdedd3122deaf7995144dbb5553b7e471a`  
		Last Modified: Tue, 12 Nov 2024 02:34:21 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; riscv64

```console
$ docker pull haproxy@sha256:eddb02b29956ea6840f3635cfa9b762397c45fa08ccd7fbbc4d7862d775ce090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14737723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016c6bb275f932f9b60d7d5720c8f307951bc9e55d697534515ffa444b3650e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912bcc9b9311dac341d2f9998e7f1fbd54b6e8e36f756419b6bbd5e959954759`  
		Last Modified: Sat, 07 Sep 2024 19:05:06 GMT  
		Size: 291.7 KB (291669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6038f190563add9bb61aef08e82a177b286f8f88aa0fd81e4b22e6ba042a38`  
		Last Modified: Sat, 07 Sep 2024 19:05:06 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1d3b9249afd01667ff722a47f90ada4aad9f92e80f95e88e88e0d1cbb877f1`  
		Last Modified: Sat, 09 Nov 2024 02:22:25 GMT  
		Size: 11.1 MB (11073142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455c3d9875e47bb17f83cc25fdb04ce33e67a5d7ae26bf1e034ea89cf4f9320f`  
		Last Modified: Sat, 09 Nov 2024 02:22:23 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:689022abcef6d3e098fd0dadc377564c7fb473e81b876375c6fdc154e0c9d998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 KB (199271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b220a7cd6cadcf60b3d6729d0de4fc56f603f7c472523bea60a9dbd29b0cd`

```dockerfile
```

-	Layers:
	-	`sha256:1250a6b1370553c19a536a354207a0a9befb3736322873f5723585e9819065c0`  
		Last Modified: Sat, 09 Nov 2024 02:22:23 GMT  
		Size: 178.3 KB (178318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d8eac5426830a4032bc3ae638ed4d38c6c80a976cecd64bcf82f29c8c9cf1e`  
		Last Modified: Sat, 09 Nov 2024 02:22:23 GMT  
		Size: 21.0 KB (20953 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.20` - linux; s390x

```console
$ docker pull haproxy@sha256:18e39ac774b44630165807cb1485836690280a8f2bed11d491d804f2ec23050f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15446958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2ade19db46e67fb1a96eea604643ad9dd8b4aff32bf599ab47739aaec779c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13459f137d6f1d753b86c71130876fe4266bfadf93bb0d2d8ecf372114a5ce`  
		Last Modified: Tue, 12 Nov 2024 02:29:43 GMT  
		Size: 291.9 KB (291896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8887f2e8c5b61094b31353db441e32037483e5da32572db319e32bed74e4239e`  
		Last Modified: Tue, 12 Nov 2024 02:29:43 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ea282ed0c596916146041ab996f831666a1d104ea328826523d124e6ff41e8`  
		Last Modified: Tue, 12 Nov 2024 02:32:17 GMT  
		Size: 11.7 MB (11691997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c26f6411aec5e1a12f3596aa6adbbac4a661222eca85d581494c71a24cdb3d`  
		Last Modified: Tue, 12 Nov 2024 02:32:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.20` - unknown; unknown

```console
$ docker pull haproxy@sha256:0d47e38eea57092cb7da56371f93709cdc709271e6326ccb08887c4fd4b4959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 KB (199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe36f8738dc30d3e314791c4f13295bb33d08604839c884fa465945dfe2235b`

```dockerfile
```

-	Layers:
	-	`sha256:ae4886d9dc57a62dbc38a28e3ea497ce836b0ffd1ed10e4f6a87785815d25ca3`  
		Last Modified: Tue, 12 Nov 2024 02:32:17 GMT  
		Size: 178.3 KB (178264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94778c17c222f49b4d78bb6cfb40871cb50bbbce52017ed172be296f21eed0d`  
		Last Modified: Tue, 12 Nov 2024 02:32:17 GMT  
		Size: 21.1 KB (21074 bytes)  
		MIME: application/vnd.in-toto+json
