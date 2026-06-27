## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:820658d9303227313f1feb164443f07319d604fed68982c918611dcaea8fb775
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
$ docker pull haproxy@sha256:69faaec78c1f50dc27184999e2ba82c07a3dc6dbda1d36343f7a092d8aae33d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20422695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103f3270314d8eb96ec5da5cfecd1090ef1770cbad88db07696ef4ad1cfc2574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 23:26:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 25 Jun 2026 23:26:17 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:27:01 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:27:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:27:01 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:27:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:27:01 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:27:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:01 GMT
USER haproxy
# Thu, 25 Jun 2026 23:27:01 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:27:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66afddb3c086cfc3a4b5dd917c4cd03cafdcabf04dd9c2c2b143f216d323281b`  
		Last Modified: Thu, 25 Jun 2026 23:27:08 GMT  
		Size: 786.0 KB (785968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a60b9111be7f23758337b6aec2817d75c91fa69b6c0c87110c7fd5579dd1f1`  
		Last Modified: Thu, 25 Jun 2026 23:27:08 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be01ac06850296401ae16c2dca94c407080ee508d9df6f39bc8cc3c39248d69`  
		Last Modified: Thu, 25 Jun 2026 23:27:08 GMT  
		Size: 15.8 MB (15788901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8310864dbce90dbf3d6780c4c2929ceb7588c9018842a6717d4bc349a0a1b1`  
		Last Modified: Thu, 25 Jun 2026 23:27:08 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3dc8e4d1d40644d90bfbac82610a28d01df31aa9f9619283f63bdb42201ec9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 KB (230808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97641cdd2adb120648d5f003a49b5aecdf7f4d76dc1d6aa4e11e640aaef7906e`

```dockerfile
```

-	Layers:
	-	`sha256:192d3be40b58f247c1ce7533647e2a8c8d4a0bbf944f59f2440c3f74297ba407`  
		Last Modified: Thu, 25 Jun 2026 23:27:08 GMT  
		Size: 209.0 KB (209015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59bc62fbb4e92c5457b22cd98b65803509e0b2d8aeef9a31ad7cc3a9dba927f9`  
		Last Modified: Thu, 25 Jun 2026 23:27:08 GMT  
		Size: 21.8 KB (21793 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:aa9ea6572eaf8ae758fd6837736961858b19779b276dfacc68fdb5dd12ba9552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3c3e8a5aeb6228aa748162aa70d2bf06a85d24b31bdebe7efeb56e43249cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 23:25:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 25 Jun 2026 23:25:44 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:26:35 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:26:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:26:35 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:26:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:26:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:35 GMT
USER haproxy
# Thu, 25 Jun 2026 23:26:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:26:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16163cdedf8006ed8be2f115b50bcf8428077375accb4f3841bfe301229ea4ab`  
		Last Modified: Thu, 25 Jun 2026 23:26:40 GMT  
		Size: 777.7 KB (777656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6174a0938c2de179ad99c20d1d1c0b4ebee6ec46c7f634cb2be972aa7790b1`  
		Last Modified: Thu, 25 Jun 2026 23:26:40 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3c70aab739502de4c90109fcff27533bf3b5ab177a547e1416845fb288b148`  
		Last Modified: Thu, 25 Jun 2026 23:26:40 GMT  
		Size: 16.0 MB (16037868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f799100e0055d976dedba3679331efe14a81f23bf04932ed255d2872a84ebf2`  
		Last Modified: Thu, 25 Jun 2026 23:26:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:26dc4ca2a0526a97b5e42a6f519748c8a343b6a97584c3cabca10668c8d89477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69708eb0635aa1d0f14cd7723da7267543989a98fb70d3b6156ba20684cbf97f`

```dockerfile
```

-	Layers:
	-	`sha256:3d42dd2dca8526e675f4e30ef658075b601250d73214400ee9b507b70d0ac7ba`  
		Last Modified: Thu, 25 Jun 2026 23:26:40 GMT  
		Size: 21.7 KB (21716 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:ae869d3bf00b8d9f294915a756d4ae7400fe63c55079911c8451d8af88cc81d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19864919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec8cf88f0a2604b927b27cec179802a5e1c7b92961241a81846080375754b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 23:27:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 25 Jun 2026 23:27:02 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:27:53 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:27:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:27:53 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:27:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:27:53 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:27:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:53 GMT
USER haproxy
# Thu, 25 Jun 2026 23:27:53 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:27:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0744edb126cbdd7f3858458f867e5a175851156a50a48aab7c86e57ec82f8d0`  
		Last Modified: Thu, 25 Jun 2026 23:28:00 GMT  
		Size: 732.3 KB (732284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819a5bd4039f0f4aac59b4b871c9c165cf37e03c160f458d6b44bf67d2e9e021`  
		Last Modified: Thu, 25 Jun 2026 23:27:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c3d6fc9697cee33f611e42e7ee4e40cc3412f2b5ac5586c04be284214c008f`  
		Last Modified: Thu, 25 Jun 2026 23:28:00 GMT  
		Size: 15.9 MB (15870585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fd9a9dea037683f90386386242c3dee2bb626e86cc49968491fc7d1139cf36`  
		Last Modified: Thu, 25 Jun 2026 23:28:00 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:2df4a7456089a83e5cad83037505cfdb1552c5e280eca0d080117717c8c53229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6def9ad4101e1de8210bd8fd08e9b9531b475420d352faae0f3c95ff342df6`

```dockerfile
```

-	Layers:
	-	`sha256:d0ff04439f3f6d3173743f8bdd19422ff9bb49ca7eaae63efa6c83ada9713baf`  
		Last Modified: Thu, 25 Jun 2026 23:28:00 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42727f168321d978f1ea14a2a3ce9755eb28a969bdd8ddf77aaca376dd0b6c6b`  
		Last Modified: Thu, 25 Jun 2026 23:27:59 GMT  
		Size: 21.9 KB (21931 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ab6ac1635f3419ef88f702d1ad51cd00f5152371ac990f33fdbb408e0aeff5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20533995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ec03cb04c50381076e208e75206d03cf9b8920a641ebdba7bf5d138ee62825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 23:25:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 25 Jun 2026 23:25:51 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:26:36 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:26:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:26:36 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:26:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:26:36 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:26:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:26:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:36 GMT
USER haproxy
# Thu, 25 Jun 2026 23:26:36 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:26:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea642869732aae7bbf35cbed938ffbd419ff6de6fffdfadc657665c7dc9553`  
		Last Modified: Thu, 25 Jun 2026 23:26:43 GMT  
		Size: 799.2 KB (799184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e0b060946ac2c6e0ce37602d2458574c82d61f55dd3cea16b3b9488cb33148`  
		Last Modified: Thu, 25 Jun 2026 23:26:43 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3085241c42deaaeb29b0450eab125426d7814b4169e958d149795e8fb70d7a07`  
		Last Modified: Thu, 25 Jun 2026 23:26:43 GMT  
		Size: 15.6 MB (15550334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399c249f2ca1be8a6c06757a71d52ff1fd082aaaca96ef6b1fc85c68a5bdb7d`  
		Last Modified: Thu, 25 Jun 2026 23:26:42 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:68352f7e21a1d04e641d4f11d1fb8c0ebaa284ae50255d6f5756b851d44ff222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ed72827af28a5b5354eeb5eaf75b117bd70976455d93f891bf07aaa5002c6a`

```dockerfile
```

-	Layers:
	-	`sha256:18d7d4ee6c62f3b458df3d76a088eafd9aa71484fc71842d06c40751933c4e72`  
		Last Modified: Thu, 25 Jun 2026 23:26:43 GMT  
		Size: 208.5 KB (208469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48bbdb31d97d1f80b8f4534b77facf719659f9c55073e8644208c6efa50299ef`  
		Last Modified: Thu, 25 Jun 2026 23:26:43 GMT  
		Size: 22.0 KB (21974 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:30ab1960513b0b3dd83ac36df474aeda031c1284fe7c7cc2d4ee72e8092b7adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20030087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35eafce1d88487d83b884a358395bbc7fd0d3cfab8e25c10ef1ad9e80c2f1c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 23:27:11 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 25 Jun 2026 23:27:11 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:27:59 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:27:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:27:59 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:27:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:27:59 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:27:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:59 GMT
USER haproxy
# Thu, 25 Jun 2026 23:27:59 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:27:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fac4e851df110bb0b0439eb6b32b927f03b3e0564f2cd4d4cecd0a00c3eeac8`  
		Last Modified: Thu, 25 Jun 2026 23:28:05 GMT  
		Size: 790.9 KB (790882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad76887c382c25a6305a125d3ed3935b72702989fff31fa5437854fbd5b45d7`  
		Last Modified: Thu, 25 Jun 2026 23:28:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e0ffc672c1b4b157f8d6912ad1f64960a343bebb0e03926812eca1b8ae5b3e`  
		Last Modified: Thu, 25 Jun 2026 23:28:05 GMT  
		Size: 15.6 MB (15567628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e93be5133bcdac2f6b672307b03e218dba6669e6b518763aeac6caf012c89ff`  
		Last Modified: Thu, 25 Jun 2026 23:28:05 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:51989c7be5635881bd97c149218e021524bf172b5db5749d9d07d82092cc0185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 KB (230707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2ea5bd8fc5212cc89c9b88919423a2a55ff83091d73771fdc06d017d327cb`

```dockerfile
```

-	Layers:
	-	`sha256:b80525528fff1ec31764c7ac87ceae859d1d0138d25bc4703924d4985dfe6fb9`  
		Last Modified: Thu, 25 Jun 2026 23:28:05 GMT  
		Size: 209.0 KB (208970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48eb0df2d21dad76dad317024b9632e87ada6c338822444393b7c63d5d8f206e`  
		Last Modified: Thu, 25 Jun 2026 23:28:05 GMT  
		Size: 21.7 KB (21737 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:dee775cdda9798ce564fdc2a774388657a37454743756a00e50d722ddee18ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21249939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8acdf209eeb83729e70f520f9bdedf887d3027bd512a18efb89a62e585898e5`
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
# Thu, 25 Jun 2026 23:25:33 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:25:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:25:33 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:25:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:25:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:25:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:25:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:25:34 GMT
USER haproxy
# Thu, 25 Jun 2026 23:25:34 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:25:34 GMT
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
	-	`sha256:3f893520d3866db4bc37ba90add6f247e0a27a75f02f03818fcf3e65c08b8e06`  
		Last Modified: Thu, 25 Jun 2026 23:25:49 GMT  
		Size: 16.6 MB (16614265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1089c21913633730f8b62784ffe7c5fc6c4f11a95269543cfaebcc126e1b0849`  
		Last Modified: Thu, 25 Jun 2026 23:25:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:1306c1f4ef0940f8411934c776f9113c00868f9a41f2a0c60c27391ab8a50472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 KB (230286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba953357f75d5f1a88f5bee210695605fd3e27b60b69b534548c0b3daa28636`

```dockerfile
```

-	Layers:
	-	`sha256:5b82db9017c2c636c747b0af891949cda41201ab5058ad9013b82f2908b04bd7`  
		Last Modified: Thu, 25 Jun 2026 23:25:49 GMT  
		Size: 208.4 KB (208422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e48f8791737259eb27da6ccfca2a8d82bd297b622c82f5ef631353ca0d09b647`  
		Last Modified: Thu, 25 Jun 2026 23:25:49 GMT  
		Size: 21.9 KB (21864 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:d2d8c8f59edfb6d805f07d0f7550fe8569ded0e2281c46f5d55720ec11a235c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21386077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac858749812ec1affb4b976e30aab77c25837e8d31836ae15f0313ea83ca5a0`
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
# Fri, 26 Jun 2026 22:59:46 GMT
ENV HAPROXY_VERSION=3.4.1
# Fri, 26 Jun 2026 22:59:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Fri, 26 Jun 2026 22:59:46 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Fri, 26 Jun 2026 22:59:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 26 Jun 2026 22:59:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 26 Jun 2026 22:59:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 22:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jun 2026 22:59:47 GMT
USER haproxy
# Fri, 26 Jun 2026 22:59:47 GMT
WORKDIR /var/lib/haproxy
# Fri, 26 Jun 2026 22:59:47 GMT
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
	-	`sha256:119578a405eba37c91bfb0cabe5474b9ba66beec11bfc18d3d8188b767d18671`  
		Last Modified: Fri, 26 Jun 2026 23:00:46 GMT  
		Size: 17.0 MB (17004577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca4475031af0876f15ebb6b1a15ee217d26730fec2feb00e66ed320b28642`  
		Last Modified: Fri, 26 Jun 2026 23:00:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:f1d148e91a807bb880c32293c626620463d85d6d4129431db400093d7d52fba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 KB (230283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ded98b1df674e4376c643955a32b142e679719ca65c34a6e82bc1f1933fe929`

```dockerfile
```

-	Layers:
	-	`sha256:7774a9e2e6e03385d6b502394024b857cf12e0f62ed11ec35b14db10a982dfc9`  
		Last Modified: Fri, 26 Jun 2026 23:00:37 GMT  
		Size: 208.4 KB (208418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:565b0e53b701e0242efc6cf197c331f365ffeba1a21011963a0170c13998ca7f`  
		Last Modified: Fri, 26 Jun 2026 23:00:37 GMT  
		Size: 21.9 KB (21865 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:c311589da8d84bfc37a47d5eece59cd040d8c0e5903ffe6b1de75675ad7ca3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20769918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd30584a9e3cf8617c02856553e0a7ee756bbb410e222610fc360057c8c50ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 23:24:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 25 Jun 2026 23:24:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:25:43 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:25:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:25:43 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:25:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:25:43 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:25:44 GMT
USER haproxy
# Thu, 25 Jun 2026 23:25:44 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:25:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616efa208e833b950093b35590102f230e67a73ed820cda91f031b325b0e07c0`  
		Last Modified: Thu, 25 Jun 2026 23:25:54 GMT  
		Size: 848.8 KB (848829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f326e5a9359d183e059c5e9ad1389f2dc5df7c9f10d31be7187a5c141b484f`  
		Last Modified: Thu, 25 Jun 2026 23:25:54 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf6f254428f612aca6a69f5e4d13eca6f8dbeca2c4ecb520b75e331bbc4129f`  
		Last Modified: Thu, 25 Jun 2026 23:25:55 GMT  
		Size: 16.2 MB (16210329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db428f15f818415e44a0274e0efaca8d4da14fa575dfd84b11e03b5896afd6c0`  
		Last Modified: Thu, 25 Jun 2026 23:25:54 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d8df44c7bb03eb8ee46372aaed29e32e7d6d52edee31afee904dbe796baa5c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 KB (230157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1847ff616a49379c6964b0a625bfaa483bd3a63e66445b5070b403dcf3f52c5f`

```dockerfile
```

-	Layers:
	-	`sha256:fd5cef2cc4ba0496edb717f82bb24ca3c17559872bca80d1a467c5cc51d4b1a0`  
		Last Modified: Thu, 25 Jun 2026 23:25:54 GMT  
		Size: 208.4 KB (208364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b157e422923665b4e25aa7ba4c1474331e81bb96ab05d09bdf9a74afe35c8d50`  
		Last Modified: Thu, 25 Jun 2026 23:25:54 GMT  
		Size: 21.8 KB (21793 bytes)  
		MIME: application/vnd.in-toto+json
