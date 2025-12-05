## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:14fb0291d1821c87c6b264f2e5797766f6f9b98ac2b9e9ac714ca3f15c810685
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
$ docker pull haproxy@sha256:2f27dd2fa61f3508140ec9b54fb273a2e443a6c3caf109e59cf66ea3f0ca45a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15799731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70915706080f92c903a93862dcd40ef2713b330bd662b15c35041ef58eb0626b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:15:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 22:15:56 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 04 Dec 2025 22:16:29 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 04 Dec 2025 22:16:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 04 Dec 2025 22:16:29 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 04 Dec 2025 22:16:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 04 Dec 2025 22:16:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Dec 2025 22:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:16:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:16:29 GMT
USER haproxy
# Thu, 04 Dec 2025 22:16:30 GMT
WORKDIR /var/lib/haproxy
# Thu, 04 Dec 2025 22:16:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c6225d21fb989d1437b654782d30073bc4608d489ab8ab3bdbf6fcb886f265`  
		Last Modified: Thu, 04 Dec 2025 22:16:42 GMT  
		Size: 829.6 KB (829631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b7934a3e8d21137ab4c8f0c05556eca13af120a62eb390004699e990230e13`  
		Last Modified: Thu, 04 Dec 2025 22:16:42 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1975ee1acaf0c323aa8a177d4aadd5ffccd2f306969f995d2e49be3b86e7006`  
		Last Modified: Thu, 04 Dec 2025 22:16:43 GMT  
		Size: 11.1 MB (11109353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988f43760d702220340b81dbc282c09b7c2b8f51b1028daf1107c8bea8842234`  
		Last Modified: Thu, 04 Dec 2025 22:16:42 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:1c76f69c966df47921b24a679ebeff11bddac5566ab29399ccaae31af9e91e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bba05e847a79c27c447e7e43c8c354502c9dbf654948ee1632b4efc0c9494e`

```dockerfile
```

-	Layers:
	-	`sha256:ea2bd3fce2ff6136abfd26f84ebdb35bda7bf964ca5a20a17ee850ab01126196`  
		Last Modified: Thu, 04 Dec 2025 22:58:43 GMT  
		Size: 227.3 KB (227322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32c62db43fb5fbf40380b904e2d62f7d1e9da96b2bedd5f70c6717ab45567504`  
		Last Modified: Thu, 04 Dec 2025 22:58:44 GMT  
		Size: 20.4 KB (20448 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:6bfe9052fbec30dc39df049a939adfb4769283be904239752cbda79a02ddf458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15606540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa1cd5745a5505ea99d1fb71c2d6a81f858cf3482107c20b001cf91d7abe6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:16:16 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 22:16:16 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 04 Dec 2025 22:16:52 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 04 Dec 2025 22:16:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 04 Dec 2025 22:16:52 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 04 Dec 2025 22:16:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 04 Dec 2025 22:16:52 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Dec 2025 22:16:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:16:52 GMT
USER haproxy
# Thu, 04 Dec 2025 22:16:52 GMT
WORKDIR /var/lib/haproxy
# Thu, 04 Dec 2025 22:16:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2e0a71cbb085f1a62229848b368cc48b46a32f2e440753b4bc41307da25f17`  
		Last Modified: Thu, 04 Dec 2025 22:17:03 GMT  
		Size: 821.9 KB (821866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f69d129fbd52251c47c06abfd80a7f3197ae9e1e8c841e55170c21e2096273`  
		Last Modified: Thu, 04 Dec 2025 22:17:03 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb1a1dbf30a1aed05827fdaef25c3ad44fb3cac5c05ea4de2c671428f37fcd4`  
		Last Modified: Thu, 04 Dec 2025 22:17:04 GMT  
		Size: 11.2 MB (11215347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f743e3808b39157100706e85da8b2a815c1dbaa9721891bf85fb0cd2b541d61`  
		Last Modified: Thu, 04 Dec 2025 22:17:03 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3e942444abc2dd112bff2ce9e855fe3572635ee776c8fb8b73e4c33126fd70d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d9af26572883d9421e4f6f254ed59202912810ffb4c51f66e8c101498085d8`

```dockerfile
```

-	Layers:
	-	`sha256:a9ff0810e43efb7790fcb0c7cf79a1ce9854feb98695bf93fe2532bf24583467`  
		Last Modified: Thu, 04 Dec 2025 22:58:46 GMT  
		Size: 20.4 KB (20355 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b1bf6b795fc1ee7702a58f6a3a9f604c29fca4551b153be1ddc3f30a5c626773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d9c91011df84f3aee200490c8b265dcd453c81a4d9e6953df05b5d514a74b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:16:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 22:16:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 04 Dec 2025 22:16:39 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 04 Dec 2025 22:16:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 04 Dec 2025 22:16:39 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 04 Dec 2025 22:16:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 04 Dec 2025 22:16:39 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Dec 2025 22:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:16:39 GMT
USER haproxy
# Thu, 04 Dec 2025 22:16:39 GMT
WORKDIR /var/lib/haproxy
# Thu, 04 Dec 2025 22:16:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82133a2f5edecbcdb6546961bd710f403fb1900a86256a7ce1e01682ca438c4d`  
		Last Modified: Thu, 04 Dec 2025 22:17:02 GMT  
		Size: 777.7 KB (777704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35786752c664122e4915b37b2936defe8370ec16b9c79a53862f604c0b46776c`  
		Last Modified: Thu, 04 Dec 2025 22:17:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a751636bf7bb3f1fdba9e1094e05e6d1b2b7525807c69c084d04873219ce6d2`  
		Last Modified: Thu, 04 Dec 2025 22:17:03 GMT  
		Size: 11.0 MB (11048781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec95b18c5719df74837cda159e4703b569cec57a88b8dbe8624e823909a1a77`  
		Last Modified: Thu, 04 Dec 2025 22:17:02 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:063b49228be0b03b851b997e0fabb2e00b3e9805bf67247ae16b285827426f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 KB (247294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620f23685e5dbb132a745001c75d9610c0e4353dc77aabbbab2796ffc755bf14`

```dockerfile
```

-	Layers:
	-	`sha256:f1c8b7762147e171f3dc024f18bd9ab52bb03b9fe1e9529fe862d3f1c9fb0e04`  
		Last Modified: Thu, 04 Dec 2025 22:58:50 GMT  
		Size: 226.7 KB (226724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f10fafb8f0434b5550e07557d7e93a7daae4e946cd55660ebf1754a1efafdf`  
		Last Modified: Thu, 04 Dec 2025 22:58:51 GMT  
		Size: 20.6 KB (20570 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:db89e6ca27790f3c4a2b214b2ccb4449f9fb0f43ae5743ac1d3e1e038209bb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16003369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ecdf4870e886dd37eb58e4d82a05788676ba070f2677bba78024731466fd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:17:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 22:17:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 04 Dec 2025 22:18:00 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 04 Dec 2025 22:18:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 04 Dec 2025 22:18:00 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 04 Dec 2025 22:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 04 Dec 2025 22:18:00 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Dec 2025 22:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:18:00 GMT
USER haproxy
# Thu, 04 Dec 2025 22:18:00 GMT
WORKDIR /var/lib/haproxy
# Thu, 04 Dec 2025 22:18:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc431ba1e080d3ddd10ac682f177fa2fddc0596140427f35627d43619f8dcf8`  
		Last Modified: Thu, 04 Dec 2025 22:18:11 GMT  
		Size: 842.4 KB (842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8b4ce54f471d4333b29ee640d7bef33add987b83920af6e0a83989a9c8ebf0`  
		Last Modified: Thu, 04 Dec 2025 22:18:11 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba45dd537ae1a5e56d32ae96b09fac3487fbf23c2b79572feccc918ca760db0`  
		Last Modified: Thu, 04 Dec 2025 22:18:13 GMT  
		Size: 11.0 MB (10964359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b44f18b9934b1105f337314da4ed48df978218e46ae292ebc80fcd0081f1c0d`  
		Last Modified: Thu, 04 Dec 2025 22:18:12 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:e2bd2c0d49204f2a6d5c43434a4e97b8c08ba3b0aa295b8ac552bf5b18746f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 KB (247358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24140b4be49de2c9bd84735f1ec928ef121642048a93643de7a0146f53765eb`

```dockerfile
```

-	Layers:
	-	`sha256:b716430637a7fbd6a6ce83fd3c2ad49c79cd10ee689194f528ac6a66da62fa19`  
		Last Modified: Thu, 04 Dec 2025 22:58:54 GMT  
		Size: 226.8 KB (226752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98bc3c3673a5a673eec34eeda1b0a1b1559ff97ef5be3743cac78ebf4ab07e38`  
		Last Modified: Thu, 04 Dec 2025 22:58:58 GMT  
		Size: 20.6 KB (20606 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:b463c5a8d8f7859522451e6ad14b03272a5327889ffc5d3bb42c78f287539760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16844dcff6748470def4d260f28d5b4fc1a299818cbd5cadcb053f12b2844cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:16:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 22:16:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 04 Dec 2025 22:17:17 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 04 Dec 2025 22:17:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 04 Dec 2025 22:17:17 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 04 Dec 2025 22:17:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 04 Dec 2025 22:17:17 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Dec 2025 22:17:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:17:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:17:17 GMT
USER haproxy
# Thu, 04 Dec 2025 22:17:17 GMT
WORKDIR /var/lib/haproxy
# Thu, 04 Dec 2025 22:17:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc070dc02752a668f453df689e900d1b96970031788815b28c158b621c2c8a8d`  
		Last Modified: Thu, 04 Dec 2025 22:17:29 GMT  
		Size: 835.9 KB (835939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f414e7c1efb5c38a153361bb7142c074cdca1e487c074e487405fb1578d5d909`  
		Last Modified: Thu, 04 Dec 2025 22:17:29 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb09df3313b5b2f8369944c53efaf0d55d226725862772b5f580ea5922f257b2`  
		Last Modified: Thu, 04 Dec 2025 22:17:30 GMT  
		Size: 10.8 MB (10818710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3b51fbe0bf17b49b4c890851e06456a3ac5c9453cad1c253f53163e01120fc`  
		Last Modified: Thu, 04 Dec 2025 22:17:29 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:62cf3687d79fc6884eb035751cbb7e19dbdd20e8fa0889b0e31e896dbdf05660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 KB (247689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0929c2d599da556af2064b72a030fc4cbd8b58c5db96dbd8257c0806bb7cd`

```dockerfile
```

-	Layers:
	-	`sha256:52d48cb26ea93cc29bd17912d3c462e3d3ce90217ee2084f7a694433cc1fe030`  
		Last Modified: Thu, 04 Dec 2025 22:59:01 GMT  
		Size: 227.3 KB (227287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48722d169b08bb2aef3fb6fda69112b883daf87edb2b5fea49b15332e073e9d8`  
		Last Modified: Thu, 04 Dec 2025 22:59:01 GMT  
		Size: 20.4 KB (20402 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6362b5b7f609c1c34905341a03ab4799dfc4cc2d1cba4d3c74fdbf35753ea16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16508824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07f95085abeba3bdba9cf6ccd1779310fba09666d1ed61694c042f65ea47a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:13:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 04 Dec 2025 22:13:51 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 04 Dec 2025 22:16:08 GMT
ENV HAPROXY_VERSION=3.2.9
# Thu, 04 Dec 2025 22:16:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Thu, 04 Dec 2025 22:16:08 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Thu, 04 Dec 2025 22:16:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 04 Dec 2025 22:16:08 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Dec 2025 22:16:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:16:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:16:08 GMT
USER haproxy
# Thu, 04 Dec 2025 22:16:09 GMT
WORKDIR /var/lib/haproxy
# Thu, 04 Dec 2025 22:16:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b6e670fd23682098623c2666f6d8c0c3c74def5d6958dc2ddb6792ab8bbb6b`  
		Last Modified: Thu, 04 Dec 2025 22:15:07 GMT  
		Size: 865.8 KB (865805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35433bd20be28b60467a4bdea56a25a2d852275f3d616149accceae2fb7022f2`  
		Last Modified: Thu, 04 Dec 2025 22:15:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b321ca6c14814470089e15259e80e345f100e405cfa783a0d0d2f1b168df7aa`  
		Last Modified: Thu, 04 Dec 2025 22:16:27 GMT  
		Size: 11.8 MB (11814563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e96a6a29b8aa87872a0813f2cd69addd4dac5c78bb8a55ac72da18b75f5e9e`  
		Last Modified: Thu, 04 Dec 2025 22:16:26 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b544705dd2914d22062ad67bc099ed24c8fd436ede05aa9cdff692a05aa3404b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3268bd04fd50fd7cca45b32ed76b2c0e74262f7d0fbfff1ed8e0376000d316a3`

```dockerfile
```

-	Layers:
	-	`sha256:f56549ecc7a94dcf5d838169257a1396405ae05c2089dbebf03ac5b15595e842`  
		Last Modified: Thu, 04 Dec 2025 22:59:05 GMT  
		Size: 226.7 KB (226717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1470d83c5fe06cd76064c2b99d70edf509e4e0fc1b87676cf1f5d1c6a10d2c4a`  
		Last Modified: Thu, 04 Dec 2025 22:59:06 GMT  
		Size: 20.5 KB (20508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:3cd268e050bae421dbef79b615e44f520ce82b5ba0ed2d556f5ca9f5ac35c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15130367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f82be8f183d9c0d9aa55a71f10c7877c62749167de1ed14669ff9d714e8fc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 01:50:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Tue, 18 Nov 2025 01:50:19 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sun, 23 Nov 2025 00:23:12 GMT
ENV HAPROXY_VERSION=3.2.9
# Sun, 23 Nov 2025 00:23:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Sun, 23 Nov 2025 00:23:12 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Sun, 23 Nov 2025 00:23:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sun, 23 Nov 2025 00:23:12 GMT
STOPSIGNAL SIGUSR1
# Sun, 23 Nov 2025 00:23:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 23 Nov 2025 00:23:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 23 Nov 2025 00:23:12 GMT
USER haproxy
# Sun, 23 Nov 2025 00:23:13 GMT
WORKDIR /var/lib/haproxy
# Sun, 23 Nov 2025 00:23:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9253dc76a405a85955230fc525abebff2e71a420232ccafc2b7288d35027fc70`  
		Last Modified: Tue, 18 Nov 2025 02:04:34 GMT  
		Size: 837.7 KB (837706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45136c5edba2c9203b29cad2c3b64d6efcad596e92bb5367ffcad5eac6184eae`  
		Last Modified: Tue, 18 Nov 2025 02:04:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5656217962efe4f3e9c059d7062848f1d337dd3d58cae684579eca9422c26ea2`  
		Last Modified: Sun, 23 Nov 2025 00:24:47 GMT  
		Size: 10.8 MB (10775976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151198940309f087ba038954276c58d949134943d88e88de19364f3b47cf0d3`  
		Last Modified: Sun, 23 Nov 2025 00:24:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:68387829420d505ed8df0f1e6f2e91209915af9b295f6c5918509d07c57d4661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d536d00516d4512de53c32291e029d4531b9333e9e6d4dc67959a77ff9548534`

```dockerfile
```

-	Layers:
	-	`sha256:23f53bf8f65fbf979cdbddb38adb84133e70c4b889ae293e85583a01f0591fe8`  
		Last Modified: Sun, 23 Nov 2025 01:56:25 GMT  
		Size: 226.0 KB (226046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47759fb7a13190dbf6beed86ec03d211e31c96d4e7e75fb41f61b7291c12fac`  
		Last Modified: Sun, 23 Nov 2025 01:56:26 GMT  
		Size: 21.1 KB (21127 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:db452f79053477deb9739704847ba7b28953ad772555f7ba24a8e7bada72a229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f23d696310985b89fda701baf180b3c24647401548b82452ba32ba18e7854ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 23:37:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 21 Nov 2025 23:37:23 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 21 Nov 2025 23:38:32 GMT
ENV HAPROXY_VERSION=3.2.9
# Fri, 21 Nov 2025 23:38:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Fri, 21 Nov 2025 23:38:32 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Fri, 21 Nov 2025 23:38:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 21 Nov 2025 23:38:32 GMT
STOPSIGNAL SIGUSR1
# Fri, 21 Nov 2025 23:38:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Nov 2025 23:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Nov 2025 23:38:32 GMT
USER haproxy
# Fri, 21 Nov 2025 23:38:32 GMT
WORKDIR /var/lib/haproxy
# Fri, 21 Nov 2025 23:38:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad067889b8f9f9b71bf379bda014acdf6c3c0d9852c452a8722f1eeb988cd8`  
		Last Modified: Fri, 21 Nov 2025 23:38:41 GMT  
		Size: 879.2 KB (879227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb7c4829a9ff2d7836da0abf945674fc0f97253b6711801e42f40806cb44046`  
		Last Modified: Fri, 21 Nov 2025 23:38:41 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cf5b486182f2968d27d150d321fab530131844dbd8f36931223d4084215e6b`  
		Last Modified: Fri, 21 Nov 2025 23:38:46 GMT  
		Size: 11.5 MB (11452811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f2032e0e08f670519d17900ea571843cbbbe8b3187b63edb55df48129ab868`  
		Last Modified: Fri, 21 Nov 2025 23:38:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:a4365aa9dbdae5b9cf9f567dd7537fffd35680fc4e288484e5bd840f128c1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 KB (247047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c920fbaf506714daf21f82483a73288c47de6eacf8112900c5645e27fd8fb`

```dockerfile
```

-	Layers:
	-	`sha256:77545cdc8731edfa0c1c55ab2ed5aaa8183c1bd4c3b8d0d3a5c56c3c645ffd7d`  
		Last Modified: Sat, 22 Nov 2025 01:57:10 GMT  
		Size: 226.0 KB (225992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055bc95902a5356d2449c6a69f7926ba7955e68c2be7f3b3279785dbed6ec598`  
		Last Modified: Sat, 22 Nov 2025 01:57:11 GMT  
		Size: 21.1 KB (21055 bytes)  
		MIME: application/vnd.in-toto+json
