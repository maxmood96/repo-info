## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:23159b87fb5b881037532cefe7a9a515eb085fa5e251015eaf90c67cd98d4489
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:48b3df0ce3854a887b136d043a4a3c525635a60a74b4759dcbc3f60e7151bbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14450590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a997353a1dd7b118acc0b296fe9b724c16f4c549d121f9fd2bbb56c7679a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9efb5679850b265eedda967deadba5d235286d4ba759f35bd16eb4893be07c`  
		Last Modified: Sat, 13 Jan 2024 01:07:42 GMT  
		Size: 284.1 KB (284106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6cbc3f2fe7a40cd6c2b67e109abafdee1c2470cb2a5f180a30f4665b7e7ec0`  
		Last Modified: Sat, 13 Jan 2024 01:07:41 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744438b510a4128da76add6132647c726e052cc979e522ca46910acb8cc17c63`  
		Last Modified: Sat, 13 Jan 2024 01:07:42 GMT  
		Size: 10.8 MB (10756269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a02492e40ea371b0a2ab822becc9aae75cf6f261674df85ffaec27e3d7e17`  
		Last Modified: Sat, 13 Jan 2024 01:07:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:cbd8727964e2e88c6cf6d652eccea12f8cf66721177f3cf335ef2ddaf7b66aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a3d2e4c3f969c906e67fb8bc198f2dfb41955f117663b1471a2b75e8131c42`

```dockerfile
```

-	Layers:
	-	`sha256:26effceb717cb65f38bada60043f08637e2535eacab7cb285a0cf94acc32eba3`  
		Last Modified: Sat, 13 Jan 2024 01:07:42 GMT  
		Size: 151.7 KB (151741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb808d8d31f49a8159e10f34e57c2859ecbad9ec03231a17d19a32337fd2d805`  
		Last Modified: Sat, 13 Jan 2024 01:07:41 GMT  
		Size: 20.3 KB (20346 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:c4cf3a03335abb21947d4f0d96ca688db3350a5cbb304c2fedeaa554e78637b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13787096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709d8062bb104778cbf26859d0b4d4452cadac9558eede85528ae5ac2eb0089a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc4a9943214e511a08e4cbec40ee92fe894121ca8db7a4ed5a12b10f871d94`  
		Last Modified: Tue, 09 Jan 2024 04:13:34 GMT  
		Size: 285.0 KB (284964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b388930b3a733d503cc8fd2bde9778b12bb5da38370fa81f1743ef97c2d5e71`  
		Last Modified: Tue, 09 Jan 2024 04:13:34 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73344c25e26209c35c2c446b6794ec829501f55a37671a85f88591e1b1feb43`  
		Last Modified: Sat, 13 Jan 2024 05:56:13 GMT  
		Size: 10.3 MB (10335259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161f8ffc093267a85a0e086c372214abfbc75ca4809c43a31208ae662ffe2e34`  
		Last Modified: Sat, 13 Jan 2024 05:56:12 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:12d854d2118d434c197cda4de3d53d3fe06f7be3f1d5071a2141165a82bb06a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6def08a4a8883da2492738f9a10158b17a686ad194ca8ae9f3c80faae63aee12`

```dockerfile
```

-	Layers:
	-	`sha256:e825d1988a829261b62bd98b3be77f4a4041992ab0be772687434fc6553d807a`  
		Last Modified: Sat, 13 Jan 2024 05:56:12 GMT  
		Size: 20.0 KB (20041 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:e4747986a50168fc384edbad2c058484657bb7e0e760424fc3d481fac94c97d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6267265c0009b499162ce70e446f152e05fc3973239a4076991ba66e5486395a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d3d8746c2c74e5291263a3c73d258d8d04dc50d43254f98ede324e51249c3c`  
		Last Modified: Thu, 21 Dec 2023 21:16:54 GMT  
		Size: 284.1 KB (284125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8099b3dc5ea43aedd718e4730fe45011daa1058581cb300585c1401c778afb`  
		Last Modified: Thu, 21 Dec 2023 21:16:54 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6befb73a9946c31b2d14b9e9664b691bd384bc7d119d692846d2ab1d4feadf`  
		Last Modified: Sat, 13 Jan 2024 02:46:21 GMT  
		Size: 10.1 MB (10087090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548bc9e0210d16840c01861bf8e7692e882d6167ffda7f937e14606b9fb94da1`  
		Last Modified: Sat, 13 Jan 2024 02:46:21 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:33f81073704b111149daf7624458ae31b18fd47c05bd3b846229e2097cdbeca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c950a82eb2facc223a0653de3cb9dcc96ac3b81b9e7f712ed8ed108b76f672`

```dockerfile
```

-	Layers:
	-	`sha256:217e55bab30f2add8b653c0beca4fb3aa69c3c4c913ba6f8855b8240ea228166`  
		Last Modified: Sat, 13 Jan 2024 02:46:21 GMT  
		Size: 151.8 KB (151793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bcfa9e482aed53f69c0fcb983480d5ae665371cd22a4b5295e26c909290fd8`  
		Last Modified: Sat, 13 Jan 2024 02:46:21 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d6eb4f3ab42f55198b9da4bb40772470639b33be6855273815adf361eddc0b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14289543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b540980fdefb50e669222e52a3818a043c83eed0dee43eff7b54830e694fa0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fbd9aa83fdb62960cd6bc5d57aee7e24030f2c19efdbd2b510a73da6d55e4f`  
		Last Modified: Thu, 21 Dec 2023 21:18:31 GMT  
		Size: 286.4 KB (286390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3156417240324d1a1e14d4da649ed8ff9e13897121684396f4a631cfc8d7a4`  
		Last Modified: Thu, 21 Dec 2023 21:18:31 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5c05735986a9a31150dcf69bf97e12a1312042c5542594017130a509d685ad`  
		Last Modified: Sat, 13 Jan 2024 01:36:58 GMT  
		Size: 10.7 MB (10653626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514db56845862bbf9e11e49e6ef35ce0ba1a5d1b61deb4e664a1b21b2b01656a`  
		Last Modified: Sat, 13 Jan 2024 01:36:57 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ea9b0e7fc253f584c0656b6e4c2ba27c9ead6efc8a7e3fabcfbb7aaf10c852e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 KB (171950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471df9d491a3f58b4ac28af38276f17832d5e614bd394ebc8d443cc35477052d`

```dockerfile
```

-	Layers:
	-	`sha256:962e8af694b52b44ba7f81d1ecff5977d88ac615bb3103080411a7eba9273edf`  
		Last Modified: Sat, 13 Jan 2024 01:36:57 GMT  
		Size: 151.8 KB (151756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be189fb8e3d0ffea6548d2dbefaaa507909e2fa1ff51b42704ea5d10fcd271f`  
		Last Modified: Sat, 13 Jan 2024 01:36:57 GMT  
		Size: 20.2 KB (20194 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:0d622d0a3a4b839abe53d475ed4cd532759e82a90bb41c23eef9bbc1cb81abbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13909570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55409b178417cfb2629f69858eaf3e1e0eb5d56a1b2f86d0c9593c7552ef858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03f566972811ab2f9afe85c28ac8968069cceb95a279a1b3ab14eb3d7bc84bb`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 284.6 KB (284554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31f7b2f1cee241f3fce2e3e6d3e37fbe25f022c965aba451e7d20f266210cb`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8f30c2a267cc5ea1dccd006ca98642e321f7062283a337f797f623559ebbaa`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 10.4 MB (10379168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a3d190f6d65d6949eec84c3e7b0d3072efcd995e41565f67fb9ccdbf9aa04c`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:f1b639f0931c3c64fd115c0b96df11414d5ee4803fac5f069acb0402e4ea7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 KB (172009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6e5ce556c2494b6b07db043c60a808a7d4053014050744ab0269f72511851e`

```dockerfile
```

-	Layers:
	-	`sha256:4b9e651308bb1c9a66e29137b427045d058104c2319aa66ce6f02d864fc4e997`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 151.7 KB (151706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:431d556d4eb00ee8a680203ba853c751d5b58feda2472f16583087d52fa951c7`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 20.3 KB (20303 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a7d01b7b8d36694fc079a357967184ba6910f02f831d639fe3dfcfd18b574c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14689679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5a04daf82282f745329d47a2c5332abd8ede9e6b52530d410aa2eefcd0438b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98add8af217e8bc0654a56f2c3fb96087d6f2e9065f0e0140e9e67344d6e198f`  
		Last Modified: Thu, 21 Dec 2023 21:14:22 GMT  
		Size: 286.7 KB (286749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fce80216432664e5aa167af2783e26605301807281088bae4c16ec8614ce4d`  
		Last Modified: Thu, 21 Dec 2023 21:14:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6049e6d1c17d94aa54ce685949339ce258c64038a05bbf50bc5a5cb5048d7950`  
		Last Modified: Sat, 13 Jan 2024 01:28:05 GMT  
		Size: 11.0 MB (11042959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75182e8cd728977a3afa3132d3b62894d96b86df0cb7ab2fc514eae79dbb37c6`  
		Last Modified: Sat, 13 Jan 2024 01:28:04 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b43639931e67d2db0bbe626e060d980e7d19a5e4c5c0ced5309e660c624a74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 KB (170385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be98180dd17e1bd8b94fbc5ab6489ad86492ab6d96796c5dab48a266ad1cc2b1`

```dockerfile
```

-	Layers:
	-	`sha256:06ea410201b44e29a220a0535c288423404e5885d32deda16e72697d8329f62d`  
		Last Modified: Sat, 13 Jan 2024 01:28:04 GMT  
		Size: 150.2 KB (150151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25afcbf429eb553d41fd307b03ea4255b273273a23d53bbf52f771453e28fae`  
		Last Modified: Sat, 13 Jan 2024 01:28:04 GMT  
		Size: 20.2 KB (20234 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:b1f6aac8821ee9038fc3644229f8cf686e11b9740b198ef315abd930a572f379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14252182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dba00b8089979e198641f129e100f658b205bb45c1d7f4acd6ad6e8108c6922`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_VERSION=2.9.2
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.2.tar.gz
# Thu, 11 Jan 2024 18:13:26 GMT
ENV HAPROXY_SHA256=851aee830ec28c1791246a9fd4478f643d115a563dd907f6612cc381a952ab3c
# Thu, 11 Jan 2024 18:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jan 2024 18:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:13:26 GMT
USER haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jan 2024 18:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109edadf9cf9d61de46da008672376ee510e24bb92e48c96f87940826ad7f348`  
		Last Modified: Thu, 21 Dec 2023 21:06:24 GMT  
		Size: 285.1 KB (285084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7d9f59c43d7c3431b235d64de5c1bc635ee4c102a6623c9be89f4f9eba654`  
		Last Modified: Thu, 21 Dec 2023 21:06:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca30d8e595bcca9b83a3440a709c206b53965229e98a3fc533383768b947371a`  
		Last Modified: Sat, 13 Jan 2024 17:23:12 GMT  
		Size: 10.7 MB (10723036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d997195d1cf25c76121f8009abb3c5559fd941e97e486701c46d9d7dd3e0465`  
		Last Modified: Sat, 13 Jan 2024 17:23:11 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:41d4f4a44d784da8167e3fcfe4e88c5fac476f00245cef82e11f511ac0589be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 KB (170284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4d0f09c3eeb197bd41e1108f91703f56dca6c15ccf14d038b63756852f8db`

```dockerfile
```

-	Layers:
	-	`sha256:0553e0699f88499d2866091ee6b07946fbabf49452f17bfdddda84a7b688e17d`  
		Last Modified: Sat, 13 Jan 2024 17:23:11 GMT  
		Size: 150.1 KB (150105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9adf1c8207777a7d79d46373460d0d1f05014a5a72834435145889b4a062687`  
		Last Modified: Sat, 13 Jan 2024 17:23:11 GMT  
		Size: 20.2 KB (20179 bytes)  
		MIME: application/vnd.in-toto+json
