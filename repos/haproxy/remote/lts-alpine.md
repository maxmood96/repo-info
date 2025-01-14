## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:7965ed622cc3be1311e9fc52c70a3f509b6bdcd9601f2b83e4eac05c3f8d829b
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
$ docker pull haproxy@sha256:88b680ca0a273a127bff2238966e70f63d01a54e9e9437f6ea1cd729ede16115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13333683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad84c12d3a151614c24f663200632baa378100b1667ef80f4d03d21a091edd6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95017fccf9e80da6b6e25381775eba104dba17e3ead8c9655639971750344439`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 294.9 KB (294875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746cbb4879d2b5ab6a20d5f6539f471d58d428cf8ab26f3ee64866e77174786`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224caf528ff9e80ae2d08cf49f73f26a289df562a800f11417404ebfff24537d`  
		Last Modified: Wed, 08 Jan 2025 18:00:30 GMT  
		Size: 9.4 MB (9395641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3d4ffc156b4ad8c78f744b10e51cac7b1219fcf32b8c760d9bee2dffdbf0ac`  
		Last Modified: Wed, 08 Jan 2025 18:00:29 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b85d68ae01362dab76171e13f4cc01d07da981478d1d65b7ae1d2b70759c2455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 KB (206811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc528a7ca129a76d8791d9f23665a0393ca3a314d18a1f8105debbd626f87098`

```dockerfile
```

-	Layers:
	-	`sha256:9783b6bca39185e359183213147ee7dce3ac8c3315531d444009b833fb1895b6`  
		Last Modified: Wed, 08 Jan 2025 18:00:29 GMT  
		Size: 186.3 KB (186349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f719305a19b2db0bd08b6661e3613c53baf61e1807b3895d211da4908f681f96`  
		Last Modified: Wed, 08 Jan 2025 18:00:29 GMT  
		Size: 20.5 KB (20462 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:f74b8226407357bd3bb81e8247dc1c79eef18036e7983d679286f85137cfc1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13042446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649765f25990b3aa1147f373ed2239b02697fef5368fb768ef0f53ec6a5d8b31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d556a8324f562d2f446b9d24c8d3dd4a29e02eb32520ce3d54310e444112f52e`  
		Last Modified: Wed, 08 Jan 2025 18:36:02 GMT  
		Size: 296.2 KB (296246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d95f458ce21e6d2cab7ca5d5dfa28cdd4998fe37ee093a32d7a6a01b09294`  
		Last Modified: Wed, 08 Jan 2025 18:36:02 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14cbdf421c0c523c627d56b2d2f1350a98d2d8ec21c4ebd528cc1b1b6f28543`  
		Last Modified: Wed, 08 Jan 2025 18:37:44 GMT  
		Size: 9.4 MB (9380870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80348fd2b4a109715fc0545a800ab74b15963cda3a35d251a265e51660be110b`  
		Last Modified: Wed, 08 Jan 2025 18:37:44 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:930601ce7e4ffb1e1e58d01d18f37be184e31ed4a370038121119da2776ad43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90efed4a6768f1b66127a8928d161ba9ec989430e2572949f6e53b033f037267`

```dockerfile
```

-	Layers:
	-	`sha256:cd919a581226b1a0b2175cdd0a089085519b2f2d3c336a70899c09672923a8eb`  
		Last Modified: Wed, 08 Jan 2025 18:37:44 GMT  
		Size: 20.4 KB (20366 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:83bfb6f2eaa84aef7bf0763f9b6498836b7d938732e3cec846c819898e689cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12633372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b80b6a7c72394be98fb74079713fd789f7c3e68067e467238153b28388784a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e60494f3a6f4fc90213d93490b73d9f826b0a236450965a2a8a9ddf0983184`  
		Last Modified: Wed, 08 Jan 2025 18:37:22 GMT  
		Size: 295.2 KB (295179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd6a50d68331a3f8b6a29d2f12b3fe60034894895af0654f0fabf555c0c16bf`  
		Last Modified: Wed, 08 Jan 2025 18:37:22 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d7480fe4a22d43622748a0742ffac1e52fb6b9bd4ac72d4bb72b4e757ed990`  
		Last Modified: Wed, 08 Jan 2025 18:39:15 GMT  
		Size: 9.2 MB (9239631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65db8726b40ebb8456618e6f0d3ac1f71264ac88b841dc079cf0b15ae47d9fcc`  
		Last Modified: Wed, 08 Jan 2025 18:39:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:6a02f27ee4a14383e32cfdb32a4d977e3e8cadf7927edd9ed35f0b215be80ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 KB (206982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e6f293eacea57533b0994b26ca5e29b59038bfbafc5e98b9f96543e0a636be`

```dockerfile
```

-	Layers:
	-	`sha256:f75a6a9f499e007d480b0753330c7c7a38836f5a9d93971f50a3c31c4930fb1c`  
		Last Modified: Wed, 08 Jan 2025 18:39:15 GMT  
		Size: 186.4 KB (186401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6caabc5f7a9a2f14ad6a792abc0e45871af6b29d052155dc6b403e007d9a738`  
		Last Modified: Wed, 08 Jan 2025 18:39:15 GMT  
		Size: 20.6 KB (20581 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:823148c4c4155b6c6956eb923bf37f95126f561c119d4a5d7d1901d0974d7ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13644487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37b26827a296322024ad0f7a6ac20ec2e7edab0d657b3a95060fed6e3cc4af6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da4c4f13d465477cfc36e0cab1cbe9cfd429b81ac4bab1a5a10cb1d9cea696`  
		Last Modified: Tue, 14 Jan 2025 20:34:21 GMT  
		Size: 297.8 KB (297845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194795cd5c08117379fc83096558010b6c0741544fc00e990b38c62c273877a`  
		Last Modified: Wed, 08 Jan 2025 18:34:15 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f541afc0136aa1e942a35b9f1a4d6dcb939e758b443bad8638a4680a3a5604`  
		Last Modified: Wed, 08 Jan 2025 18:35:44 GMT  
		Size: 9.4 MB (9352834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c6ee089040387ad590ba719105b9eef42d67d43f42fe0e5409662da7472a5`  
		Last Modified: Wed, 08 Jan 2025 18:35:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:87f0f912b3e06b05fe5257d05121fec1f55221a339a80697cae200e016011e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 KB (207050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3aebf7b70a2ea5eb8c72af436bcc6506d3d2d452c3e332ecb20dbfa54e65d7`

```dockerfile
```

-	Layers:
	-	`sha256:3d656e493660b9c50112c73fb815ceefb9bdf9a964a9c25d8ae4450c415a648a`  
		Last Modified: Wed, 08 Jan 2025 18:35:43 GMT  
		Size: 186.4 KB (186429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4433fe67848e96a6b6ef8e6ae65fa45772697ab66b33e4c578bf5b5a62c0cfbe`  
		Last Modified: Wed, 08 Jan 2025 18:35:43 GMT  
		Size: 20.6 KB (20621 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:fb6ba782a3222885f7479048c7e4df57fc2f93a8bebfda292c04b647f43fae8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12923253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1dcdf05ced30d5260dfdab39259b3fee71e8b72b29863b19393e8352af1239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9804b7f7db40bc0f2bc72f2939c01aeda3e094b9aa414c75d82fd84dc611e4`  
		Last Modified: Wed, 08 Jan 2025 17:59:07 GMT  
		Size: 295.6 KB (295576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21dcd637b4dd71fa1ad41e45d4b9cb9010526c16cd69031d0188a66a544c561`  
		Last Modified: Wed, 08 Jan 2025 17:59:07 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78251881fde0a182cc2204e70655aa4d2b2ff5472f987f8631c8101e5ef54d23`  
		Last Modified: Wed, 08 Jan 2025 17:59:08 GMT  
		Size: 9.2 MB (9163105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3074c4ad8683d63732b2a526cd12d87bdb843787b30721c963a70e3e340a9414`  
		Last Modified: Wed, 08 Jan 2025 17:59:07 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:5c1849b69c4054a8c8d4fb28b256ed2af1b2a41c78b6a86c38447ff8e99b30d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 KB (206731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceff06917de9e73eeaab292427bfeb4b8dc920c24a56fc96827212df62bb967`

```dockerfile
```

-	Layers:
	-	`sha256:fbabf14af9e710cab2684dab2e89cd828e1c7120a48c283d92ca4532f6f7ed08`  
		Last Modified: Wed, 08 Jan 2025 17:59:07 GMT  
		Size: 186.3 KB (186314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130d0689765d1073d1a12e9cf68190e055149f0caa58a852f64579c83925bf5b`  
		Last Modified: Wed, 08 Jan 2025 17:59:07 GMT  
		Size: 20.4 KB (20417 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:41973934df3ffdc2dca1e4d8418b6cb3e5025325e9b871828bdd0f18cb0e2d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13775797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e3a8dba4e0bdb2455b5c9be48e17ebc77183bb6cf065263d010ff3a8ba19b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f362dd4906448cab5e72811bed0918e1b07a8c86888125930bc35adc0798da10`  
		Last Modified: Wed, 08 Jan 2025 18:18:15 GMT  
		Size: 298.3 KB (298268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7214435fea52fbbcd213ccb12857a27a1c1caa75e3d2a6ccb55eff0054df9d`  
		Last Modified: Wed, 08 Jan 2025 18:18:15 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c206f1e489b1f89d805269ec13cfd0b3ef973e2375e4c4fb5f9a7d6dbe443b8`  
		Last Modified: Wed, 08 Jan 2025 18:19:48 GMT  
		Size: 9.9 MB (9902479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d272a139d5745e39199b2007abfd40e7a54d5c4d7c7f566c86840c841e81e361`  
		Last Modified: Wed, 08 Jan 2025 18:19:48 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:437872440c80ccc49b75c622f17a99f852e6f0ec2c507f8f88034429bb35b76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 KB (204967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb211947f0781266cde1abb5b3815ed43ae322fbe0245a34290aa2465a95218d`

```dockerfile
```

-	Layers:
	-	`sha256:cca6978fbad598723093d7dbdffa0004012c3dc4feb8f664fa7ef9dd900f8f08`  
		Last Modified: Wed, 08 Jan 2025 18:19:48 GMT  
		Size: 184.4 KB (184444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcec6e88af0e0eb7d29db63d9f1d56c149b35a12941df2d387941d5d8be0432`  
		Last Modified: Wed, 08 Jan 2025 18:19:48 GMT  
		Size: 20.5 KB (20523 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:0358a2e31a193cb68e16eca745b5bbcea4b0dff8fde02ecc91ec472e36b55c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12711050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cea371ff776530e961b816f38c26d9830618a3c810ed39d814cc285173c629`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e2572b96227a52f0bf0178e3c46cae1bb0a60fcdb0179714dcd2b43c365ab`  
		Last Modified: Wed, 08 Jan 2025 20:02:41 GMT  
		Size: 295.3 KB (295336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50266b975b2ac4b18eb24f95cad91ce4bcb7a5ade1e6e98501cec6b08fa006b6`  
		Last Modified: Wed, 08 Jan 2025 20:02:41 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f81a371439bf6c32718e86be8989664bb98862cdc169b1e6e060c2f114a6faf`  
		Last Modified: Wed, 08 Jan 2025 20:25:58 GMT  
		Size: 9.1 MB (9064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ef1787343545063bd0f911630d77953509302055a0e27f0dc78c60eebe5a5`  
		Last Modified: Wed, 08 Jan 2025 20:25:57 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:dad165e1decdbc95d09f3bc6deed2d6787fc10a4f28a2a2fde48bbde0ff05b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 KB (204962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16038cb69e9140911b234a761d329a4b895acc42eb65254fb42ebe1d183525`

```dockerfile
```

-	Layers:
	-	`sha256:e8103ed997010511d3c27298205f5b9928c03190b5212e79a3892e885b652c33`  
		Last Modified: Wed, 08 Jan 2025 20:25:57 GMT  
		Size: 184.4 KB (184440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe959b620c8045125b98ee0a84742cea088fc978de0d6247faddea032fbcc51d`  
		Last Modified: Wed, 08 Jan 2025 20:25:56 GMT  
		Size: 20.5 KB (20522 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:cfc3e8d4056d2bc0fbf3335481d5e4904cb51a8686b48c1fb9f7161c5185ea21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13345949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f8c6f457ce693d09000ea85b40500c771296b32ae686cdce1847cf5e022039`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb816636710fe0bc908d632856c9e2f819fd50e8e353214c01a473f611c8dcf`  
		Last Modified: Wed, 08 Jan 2025 18:16:38 GMT  
		Size: 296.2 KB (296157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a8365e2eabcd90f7a1ec0a15ce8c9e8d15304a2ace0d7df56fd613742601df`  
		Last Modified: Wed, 08 Jan 2025 18:16:38 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ba76d58208579bb695c354d1158e0c4fc2a2126a4dfb6b0d7f704d9987cbe1`  
		Last Modified: Wed, 08 Jan 2025 18:19:13 GMT  
		Size: 9.6 MB (9581478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903f6fceb5acd4f9e89a579876ed768062cb04469eab75b53f6bc531a634f898`  
		Last Modified: Wed, 08 Jan 2025 18:19:13 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:07c0de8a846aaa1243b49e2639eba5cefd5fc1fde3680fbff6b537c592eeb14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 KB (204861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d72877790e735d0ac543ec1049ee6a17c20ba9a0e17ffbfeae94f8771a8b71`

```dockerfile
```

-	Layers:
	-	`sha256:09838ead13a685816dd35ebbe0c7fe0ea23c354127470a77bd370f7d093131fa`  
		Last Modified: Wed, 08 Jan 2025 18:19:12 GMT  
		Size: 184.4 KB (184398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b7dfdd7b305278f12f125159c3e3a42b017ebf59585057608a355b535099bd`  
		Last Modified: Wed, 08 Jan 2025 18:19:12 GMT  
		Size: 20.5 KB (20463 bytes)  
		MIME: application/vnd.in-toto+json
