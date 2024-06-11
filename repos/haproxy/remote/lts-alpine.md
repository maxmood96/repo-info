## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:4d2286feafe186bc18080456f6760d65e6f747450ab4b6f91c607da073698343
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
$ docker pull haproxy@sha256:ea583c6f82625635e2f273b04bc2c03bca1fcd9ca843a3659bb4d66d379c7463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15524767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aaea7b90589c475fe5026f6cfbb4ee2485a4753bbf3bcfe08ae52f621f6da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479a235a1325691c4e37ecbfa9e4880fdb50ff0194b4937e955f4dbde3da1318`  
		Last Modified: Mon, 10 Jun 2024 22:33:26 GMT  
		Size: 292.4 KB (292425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0530ed9fb2e59f20e20019a4b03fff6e315e8d7ed0fef04e8c7b4797bcaad747`  
		Last Modified: Mon, 10 Jun 2024 22:33:25 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd02592bcd064005c3f0e33f71ef2cfe0ffc7b22ea0f90a711f7359f55b3c1a`  
		Last Modified: Mon, 10 Jun 2024 22:33:26 GMT  
		Size: 11.6 MB (11608797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac47d0bd721319b407485776423a47020837ecdf5a3052b433991fc35bd50ce3`  
		Last Modified: Mon, 10 Jun 2024 22:33:25 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:66657871d2bffa80aa8d7aa5246f9f0afba543317d8b54b4f23d8464905c9425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 KB (197470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7a0417599d6886f8a0adcdbe317b20ae0fb0f38973a51d7e79d3185088f1ea`

```dockerfile
```

-	Layers:
	-	`sha256:7d09ecfeea66915865fed309bed19dfcae98d9b42d4da10873822671e48994fe`  
		Last Modified: Mon, 10 Jun 2024 22:33:26 GMT  
		Size: 176.6 KB (176617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c749398f7f9d8d0afca1aa33111ecab77e2548685a06d77a372cca39107f0ab`  
		Last Modified: Mon, 10 Jun 2024 22:33:25 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:b539cc0d1bc041aa93fd8ba8c43ed046d79e9925df733009ed27c6b9b891851d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0475da2f841aba8c85e679adfee9e0c4f1f8cde56becff15333145296f26a4a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6d87a31d748afa9ddec5e039b0db3020b4f4727194578756d248f738f7f7ef`  
		Last Modified: Mon, 10 Jun 2024 22:32:48 GMT  
		Size: 293.6 KB (293620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43f6567fa02dd58d083f3c159804739694b181b396511b1e2b98517f14b3a0b`  
		Last Modified: Mon, 10 Jun 2024 22:32:48 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54e326609839f1242fcba8d88c0c9d5eddacc3a5e6c49ac5c4e8cbf55a2d4c`  
		Last Modified: Mon, 10 Jun 2024 22:32:50 GMT  
		Size: 11.3 MB (11286764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728be7b00987eeee68d5292354654229b5077882365e7992b01cb9cd4872bd41`  
		Last Modified: Mon, 10 Jun 2024 22:32:48 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:5c8e8ae34d6a33b6555fc61366c26bbe53a707165beaee46820c1c1a36de450a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42d8f63fdfdbddc5618ed6a633a22ada59702d6e09f0a6c2f789657a7c59b5b`

```dockerfile
```

-	Layers:
	-	`sha256:9bb2d336b3d2f13aeb8c8d6f8fb08f104e7e121f3ab1587d87c5522a8080933f`  
		Last Modified: Mon, 10 Jun 2024 22:32:48 GMT  
		Size: 20.8 KB (20762 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:46ebfa6e048496e6f919b1e074c493db63150cfc956e8fc5c2ad70e2cd923de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14378142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84132713944d670fda4821a3938fa1f8f65e124584182507dcb01ac4fd69c9c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56f5933f29d2e3bb7cf19256d397a4d6774eaabb59930660da3c555a08f3d4`  
		Last Modified: Tue, 11 Jun 2024 03:08:51 GMT  
		Size: 292.5 KB (292467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaebea345a55ab9fa02a7c9631e24fe91423da41da58d2f8042b548b437c0ce`  
		Last Modified: Tue, 11 Jun 2024 03:08:50 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db234d9b6e39de3210e05c831132a41de3aa5902d97bd4cb56904bb6de60ec50`  
		Last Modified: Tue, 11 Jun 2024 03:08:51 GMT  
		Size: 11.0 MB (10990189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd9fb9749f514f436121e3d1adca983850322f4268953b2ffdbb09b5b1ec7b`  
		Last Modified: Tue, 11 Jun 2024 03:08:51 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:60b964650bc2e148fed8bcd7a72d1fd9e366504d55fa16996a164cd56592c094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 KB (197665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8421569e9107821187e118c3a4d90c8b41da51f0937701446477922e6596f5d7`

```dockerfile
```

-	Layers:
	-	`sha256:1e03f5d15579a3f1dfd53627059cad332503a6002012d4dfc0cd10807e1462ca`  
		Last Modified: Tue, 11 Jun 2024 03:08:51 GMT  
		Size: 176.7 KB (176685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3780610dc6b5c20116d6b549467fa8be259cbb311fd9365a26742234e6199cba`  
		Last Modified: Tue, 11 Jun 2024 03:08:51 GMT  
		Size: 21.0 KB (20980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:314efda418b3aa8460a6faf19a6ee78e543a8b7642faf87b2019b351c8c68130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4a1eaa53d306204a6ef9bb5e66bb973dfa34e710d04c82bd52c91e75c8c310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431acabf9f85735e66acf0ef97a2b133b3d6930012be068b398210eaa76b468e`  
		Last Modified: Tue, 11 Jun 2024 03:35:25 GMT  
		Size: 295.5 KB (295456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f04388b9eadabc04ca394da08a2bf859c7afb251f92a3b7c4aacc211b7fe46`  
		Last Modified: Tue, 11 Jun 2024 03:35:25 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57757796dcdfb2338fb0960ac4078fc9ebf24c7a12189a7b04bc6e9bd58a26dd`  
		Last Modified: Tue, 11 Jun 2024 03:35:26 GMT  
		Size: 12.0 MB (12030513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ab62f1d65b847139f550fd87215bcd67b1c85b754e0aa6a6cbc4848c7863b`  
		Last Modified: Tue, 11 Jun 2024 03:35:25 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:bb5d5564e6b458bad02aa5e88c73e61c8c3d448f80e0300dc91518a2f91e0ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2df05b7b7ad47361a846fbed68dd5da333dcfc5a49010d1ad22c7a649e722f`

```dockerfile
```

-	Layers:
	-	`sha256:ffb16c2ad1282cae45ae484b5122dcab1ef983053bab8845bc582801b65ef02a`  
		Last Modified: Tue, 11 Jun 2024 03:35:25 GMT  
		Size: 176.7 KB (176721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b55938be4d9496c76edf771127a983aac1bcfbcbdbde3565a0e517277290af92`  
		Last Modified: Tue, 11 Jun 2024 03:35:25 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:c0645b7b2a43f06064eadd83fbad408e0ab72598de9957c3dff050a02aa08eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14999332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c797f2e859d73aa0faa9af8be89c865fd0eee121aad6f527ee3179f7915cc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392bdb5e5c6f384dc4cdb92af5248dc92f4767a4df70c07c771575b9ceb06a45`  
		Last Modified: Mon, 10 Jun 2024 22:33:33 GMT  
		Size: 292.9 KB (292877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab0232268da883953f47e71fd3cc3aaf334b822a8eec2258fcb7280b25537f7`  
		Last Modified: Mon, 10 Jun 2024 22:33:33 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bfe900e11ef464ae72a90f4dbf25adf7146b8d98bb0c3dd9163583514997f9`  
		Last Modified: Mon, 10 Jun 2024 22:33:33 GMT  
		Size: 11.2 MB (11237824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ab2f95b05fc899cf4bf617423dcc5769711f221c6ff524953592fba25c6771`  
		Last Modified: Mon, 10 Jun 2024 22:33:33 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:08272573e4fbc8e766bcea13b42ea88436ec386065029332f372be241ff828eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba3447477be98d4878c53298fa9b7708523d9e98edc34607a97d4e3841fbb2`

```dockerfile
```

-	Layers:
	-	`sha256:61720bf5f0aad87952de38db2f968e3397701004cf12907e28ac3eaf26c80d1e`  
		Last Modified: Mon, 10 Jun 2024 22:33:33 GMT  
		Size: 176.6 KB (176572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebc220d4ebf54cceffcb4e7894a55816302b60a11fe2490b7f7155a72822b78`  
		Last Modified: Mon, 10 Jun 2024 22:33:33 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0d7be2fc875811ecea7edef7030a739211b221d094c8667468c36881e775190a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8dfa8b7e65d928a78cc02d545adfc00b4dec3e7add4d2d83155e6986567455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205b34e4839457aa1220a821e34f600a43aea330bcd67ff9e43f1d52116f9fc`  
		Last Modified: Tue, 28 May 2024 23:02:56 GMT  
		Size: 295.9 KB (295874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4193c5bc86ef2cb6bc462858d92bdbe325ffa99705483773961925419201550`  
		Last Modified: Tue, 28 May 2024 23:02:56 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f05aca8def00f834177332aa0bacf4192db63dfeb0ed452b4424764aa31a52e`  
		Last Modified: Thu, 30 May 2024 02:54:15 GMT  
		Size: 9.7 MB (9726587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304f35eb58028c93dc711b2c49ed9f78612f099c4650c8f924e6d66a563329f5`  
		Last Modified: Thu, 30 May 2024 02:54:14 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:260e45710959b711c30620523253b75b6044baf44073a8bd3d2f843f541987b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 KB (195589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e000fd25c5ec05a8e4af2540e08fff913d0eab7d2455351d8a16f8a0ab300749`

```dockerfile
```

-	Layers:
	-	`sha256:eeaa2a04552ccde040780fc34b7d5d1e02556b4878fae6cbf09c5759702a4364`  
		Last Modified: Thu, 30 May 2024 02:54:14 GMT  
		Size: 174.7 KB (174722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639d3fe504b7f10b467f6853b629d007d0aef028ad1c9dfc412dc5ff9b8f1b7`  
		Last Modified: Thu, 30 May 2024 02:54:14 GMT  
		Size: 20.9 KB (20867 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:bd38f9ef9ceaf6c75d13178a7224e5c93e9b56540405b430939c8163e792ad9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14644403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc539891de94077adb638674dbc88c008f32c4cf027ac801c98159c9b1c5812`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf326e5ad47db4541bf18551063cf389c6d8edc10b1f6856009c30ad1dddd8`  
		Last Modified: Mon, 10 Jun 2024 23:27:01 GMT  
		Size: 293.2 KB (293166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465636c8c84840fcf3deb9dc17dd0c56924cf5667b0c96fde6eeaf4081ce0a35`  
		Last Modified: Mon, 10 Jun 2024 23:27:01 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147fd59faaf6826d5b281e269ee916f4f9568b48cd75c07b7b90cff11114a2b`  
		Last Modified: Mon, 10 Jun 2024 23:27:03 GMT  
		Size: 11.0 MB (10981217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6c4f6b76053d8fcc8e8d7f223fa11bc9985ab7e5dd888b5a260f7034af542`  
		Last Modified: Mon, 10 Jun 2024 23:27:01 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:a1fc9f9b8af10ca7c104dc2831d65a4cf349f510e33ebb14bb263ad048c128f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 KB (195635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6abec3dacef05057a72e4cf7ace67cedaa2dff7c3e4f5d6961ca0d1ca4437b8`

```dockerfile
```

-	Layers:
	-	`sha256:1ee976ea99be8738415ba9a8b8096de71be45dd25aa2b54acb454e4fd389d495`  
		Last Modified: Mon, 10 Jun 2024 23:27:01 GMT  
		Size: 174.7 KB (174717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ac71b6601a024cdf3e65c02e05704e531aec4048ce1138b76645eb324dfadb`  
		Last Modified: Mon, 10 Jun 2024 23:27:01 GMT  
		Size: 20.9 KB (20918 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:92bfdac6b3bf5974c1c2b217e1d476958f1447b86dd3d8e14d0982bd74cf57a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15361360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801414b73ca0c4b23908ffedd91fd17f1e7618eb8469672bfbb161c420e46759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbae4381455255ad1c4d7bc2431abc34f8db5a3ee7220b7968fe9c600625f6b`  
		Last Modified: Tue, 11 Jun 2024 02:15:53 GMT  
		Size: 293.4 KB (293409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c442f3d8a0bf68641354d67514d271a067b561728524095203a07999ee6d6ef`  
		Last Modified: Tue, 11 Jun 2024 02:15:53 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1534bd111fa8f9cefddcdbd4d32c5087c45cec70883a9f03d7d5d9ea70b239a4`  
		Last Modified: Tue, 11 Jun 2024 02:15:53 GMT  
		Size: 11.6 MB (11606161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c1bb04ac0918ad1deed3ee56322c6325786bb7b85968df7521db8595075a77`  
		Last Modified: Tue, 11 Jun 2024 02:15:53 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:df8789c4ab96dba8b6eec67ed566d3cc012f3352bccab3d7874cd512a34975db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 KB (195516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3d6b2ab53417d84046e1f5100998c52d69c636614a293a6bc0d14ba04fbe24`

```dockerfile
```

-	Layers:
	-	`sha256:3c7e7cf7e024e6376385485b825f37dd37daf537e091db99fc4effabea1f22ec`  
		Last Modified: Tue, 11 Jun 2024 02:15:53 GMT  
		Size: 174.7 KB (174663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5bd190d29a9e3f6100c7706b05dcd833ac58bc08933de9e9c2e40c8a76d9b9`  
		Last Modified: Tue, 11 Jun 2024 02:15:53 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json
