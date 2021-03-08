## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:1acfe61b2c69a62809ba7899b3b4c8e7013e6e669073c65913eda836cd8e46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:bb0e20bf8631ecf3edb8fc5d38f32e4f8683f4bfa22ee4d3c1c19257260c3e10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9470523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c739eebc3708f3bf44ad3721798cd90428e16ce16fd7fd00e0913a0a6f911224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:42:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:42:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:42:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:42:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:42:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd249d2b29591c8718e8042dbbb0295cf28f32e5d6f2d0c6137588c835a373`  
		Last Modified: Mon, 08 Mar 2021 21:53:19 GMT  
		Size: 6.7 MB (6657113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffe9787642facf9bd36f4d104f20530c82832162f57aea7303cf18e78e18381`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76363271b801b0e06ee5b00d57f806f69f4dd16018917904e2a7366ca5d4f691`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dad539f489eddffa79e2bc62db45c170d386e7e50f3ed9764c6f2725c956d8cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9180433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1eae12a743b81699c7d83b505ab33f3215795d7f585cd5a6d85bb9f1df74595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:52:03 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:52:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:52:05 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:52:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:52:47 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:52:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:52:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:52:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccee6a4d6ac6225e6187dc0e46c70472f929133726f02d42c2cf67cf98a26f0`  
		Last Modified: Wed, 03 Mar 2021 23:55:01 GMT  
		Size: 6.6 MB (6556640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff92ae4d51d26dcd1ace6305cd0065294b2c57cb28f5cd1d5fb8c87d0eb0de5`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141ebb3c783c45f4d18a6a36fde22ab8925733991323335789c6079b8288257d`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b20ebce77cee18aa4b18109c23f165d16f1fa602087f9cc6500719a555d877f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8902072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb1f5a0f63bae55a706913af7ee4303dcd8da7ff29bd169c99425e8f8d78028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:01:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Thu, 04 Mar 2021 00:01:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Thu, 04 Mar 2021 00:01:09 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:01:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:01:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:01:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:01:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:02:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfad952fdf51b889dc5d6e3b4fd1cc4ee75e696df82fc4ab61a934b3d7d0963`  
		Last Modified: Thu, 04 Mar 2021 00:06:38 GMT  
		Size: 6.5 MB (6476423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6974c640fb0a7c93496a49eda6f453ded411da802620224ab9eabb800ac7b25c`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c686e3ab18a686bd3d0d979838afafff033210b4a23d632987958bf6819f67`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4fbb7b77eec6f9ee10edfd294837fad3e682e5b3f74c2ca24683e7fc808b4270
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9380846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd25c0078f44eca15948151ec0ff316e79f750fec9191e8f3efd49a4ff980f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:14 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:16 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:41:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:41:50 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:41:53 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:41:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:41:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc1f8d42c267e784c8b356dfea3c9253203b122ad990cd4d37ded39a0e656e9`  
		Last Modified: Wed, 03 Mar 2021 23:45:00 GMT  
		Size: 6.7 MB (6667516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a90e0b19f903de5d2fe3915f417de80c2ef7d2a56661a7e72942b224f32b86`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca444d151b0822cef49ee7729684f9ece293a9a81bc6282fc78559124d793b`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:994058b2b2ba55b755e38344adba0c31d56640911e9cd83eb7f1e87901f3900b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f000368b08b43f83fc8fb4d5dd02fdabf666bc713f749d3fc4b5e4392dd5366b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:07:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:07:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:07:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:07:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:07:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501416f7b36ee8ae1db9b34eceed0af66b127a1ce1a24b627883048028d1d06`  
		Last Modified: Mon, 08 Mar 2021 22:18:33 GMT  
		Size: 6.5 MB (6503146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5700332802e415bfca89d97df82941bdf05c6cbc177f50a7c3e96d784a508a2`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f6a4303e7e72e2141a6a68bd313e07230e8f857dda792113b4746f97b84155`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7d3892886cd28df906de4269cf803495cdc753bd3ee815e71b729ffaae219b93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9798645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb459e90ff5599695221ef998010e7da3c41f3b1d284dc8d03a34a9443ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:21:56 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:22:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:22:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:22:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:22:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:22:58 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:23:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:23:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8505b18905139bf39bbee5b1d18e7d1cd0d729fc1ea3a2630643c89f760e9b3d`  
		Last Modified: Wed, 03 Mar 2021 23:32:00 GMT  
		Size: 7.0 MB (6983804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d123eec920832dc833ae5ebe82126f063dfbf0401f32d1d47e75c54ca1829a`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea331f8b85bdb9c8c7f7c51ea304edd7fb486abda08b014da26b95bd3b63af41`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:e4a841f57598b3e66eb87c80436106cea84efd6c9d137ec28641ec8e057cb742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9227626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55a39fa38ab3d8c3aa8f4f7c6649619ad06a4445975af1730c9aa1a73805f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:26 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:43:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0df5fca35947aa6a68611a88bc3b2d7b1213d50a7776cd1460c718c970c3a0a`  
		Last Modified: Wed, 03 Mar 2021 23:46:07 GMT  
		Size: 6.6 MB (6623491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31ff14df8c306d11a15e27642d466ac2c59267055f69b77ed86ea72289114f`  
		Last Modified: Wed, 03 Mar 2021 23:46:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aea0c74922fd9cb56014cf281aeb5c1df5d59e73ca4a4694c5903d80230d3a`  
		Last Modified: Wed, 03 Mar 2021 23:45:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
