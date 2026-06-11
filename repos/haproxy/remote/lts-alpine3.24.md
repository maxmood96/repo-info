## `haproxy:lts-alpine3.24`

```console
$ docker pull haproxy@sha256:a178a95125529bdc9879a8eaee2e83edddd69b9ca298661f0fe3782461f846db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `haproxy:lts-alpine3.24` - linux; amd64

```console
$ docker pull haproxy@sha256:4d27d2c9782ee491d968faecde18c258c7b4d93fcf270f2898db8bf6be0b5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23080746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f7bf5b1264c017cac312f7f1f596068b3bd26db9b358fd066b143af55242bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:53:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 10 Jun 2026 20:53:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 10 Jun 2026 20:54:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 10 Jun 2026 20:54:15 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 10 Jun 2026 20:54:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
STOPSIGNAL SIGUSR1
# Wed, 10 Jun 2026 20:54:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:54:15 GMT
USER haproxy
# Wed, 10 Jun 2026 20:54:15 GMT
WORKDIR /var/lib/haproxy
# Wed, 10 Jun 2026 20:54:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4f90bc317c8c48ead3a455fd46dd6745aba1508a821f12b9eba4ec9e269744`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 832.7 KB (832742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d09b3e974e7a62047db2940fd0d4cce03cea8d8a643722c3456d7265d305b2`  
		Last Modified: Wed, 10 Jun 2026 20:54:21 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f697031282fd02373b716abfca12ed9c2ab112ba783da147db94b147fbc32ed7`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 18.4 MB (18379809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5077dcf236ea47d8ef907d8aaf0eb60f150b7b42127ef0d9dca822cae08b8418`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:0c29df2a84d5290016388b8ba9d9acf18fce37fbfae6e64aebde5452e5a8df45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 KB (247698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b5fe12aa3f96b7203ac1f1134a6714ea3df35e5b6f2e956c954f6b72789965`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9a9bba366b60888d1656ea7e3d1a4eab101cf65635367b55cb87f0042da81`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 225.9 KB (225907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22df9eec3afa4c9808f71fab5d34ad885d5c276d3c438ffb082bb43bd1263a4b`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 21.8 KB (21791 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.24` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:a351b60ed8ae6b957d0cebe75637c700d982f8f3eb2234cc677257be42a4aef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22674578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c00822702389401d93200ff2d7f9b6614788ea16521f03a745760a3881dbb0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:20:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 10 Jun 2026 21:20:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 10 Jun 2026 21:21:21 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 10 Jun 2026 21:21:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 10 Jun 2026 21:21:21 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 10 Jun 2026 21:21:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 10 Jun 2026 21:21:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 10 Jun 2026 21:21:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:21:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:21:21 GMT
USER haproxy
# Wed, 10 Jun 2026 21:21:21 GMT
WORKDIR /var/lib/haproxy
# Wed, 10 Jun 2026 21:21:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd64cd5c22568aa10d8981006dd7e700aaa3861e2786fe7747bd81ed8ef3888`  
		Last Modified: Wed, 10 Jun 2026 21:21:26 GMT  
		Size: 825.5 KB (825520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea96cc638d130ce4aca732a5d22a1eb6c76dff909c5b19b3538e0e6eb40c2286`  
		Last Modified: Wed, 10 Jun 2026 21:21:26 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07fef26eb1f79568861a07f5b82051b734d38d5a6853048944f031ca9525bc`  
		Last Modified: Wed, 10 Jun 2026 21:21:27 GMT  
		Size: 18.3 MB (18272311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da5fe1cb5a5ef9eb391d0b8e6aa65502c95709988ce27a9251be0aa53e6e59`  
		Last Modified: Wed, 10 Jun 2026 21:21:26 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:46053d3e91ee33be2774224c7e1e3b61cf729d15a9545f02ce945aecff8233f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78595370e77c82875d45c26cc1b4888bcea77e276ef4fc2627c34c16fed3e01e`

```dockerfile
```

-	Layers:
	-	`sha256:5d06881d3e5333d3cc5286f5e0ed9ecee9ae59d896f494bcc99a74e160819cc4`  
		Last Modified: Wed, 10 Jun 2026 21:21:26 GMT  
		Size: 21.7 KB (21716 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.24` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:ae3b4d49b1e08d642fe1c6b9e2d8cdea553fa80681b179ff8225cb8729e42c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22007439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ea45e777431754579daf5d1928d4d7eb144e94a77327b1f406a0ce95d945b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:31:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 10 Jun 2026 21:31:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 10 Jun 2026 21:32:44 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 10 Jun 2026 21:32:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 10 Jun 2026 21:32:44 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 10 Jun 2026 21:32:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 10 Jun 2026 21:32:44 GMT
STOPSIGNAL SIGUSR1
# Wed, 10 Jun 2026 21:32:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:32:44 GMT
USER haproxy
# Wed, 10 Jun 2026 21:32:44 GMT
WORKDIR /var/lib/haproxy
# Wed, 10 Jun 2026 21:32:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb96d21e8eb72221134f5fc436cd993699ffebc0f527e830fd383b967573172`  
		Last Modified: Wed, 10 Jun 2026 21:32:50 GMT  
		Size: 779.7 KB (779741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109b3dffef933d6b114ab15a955ecad634d215491536a0c63258a14efdd6f8`  
		Last Modified: Wed, 10 Jun 2026 21:32:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb50d57f6f3ec759d05d23dce36acca709282c1cefd1048f7ce37acc10ecfa`  
		Last Modified: Wed, 10 Jun 2026 21:32:51 GMT  
		Size: 17.9 MB (17940098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f18b25ff3cb14b115781da1697ee753c3f1fc7e2fa7efc0da6e6b4693ffa7`  
		Last Modified: Wed, 10 Jun 2026 21:32:50 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:75b7d2fad8feb4a34af8449b49cca92341d8b8c7b18c5faa4c0ff32cbfd85248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 KB (247256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086953b9da4a92338da701f2c0c829fb0dec8f5e07bf95ebb203ccee5303bbe4`

```dockerfile
```

-	Layers:
	-	`sha256:28cce1c60f0c7b92edaa4eaf9f106014c96537c42887330ee2104c8463eee129`  
		Last Modified: Wed, 10 Jun 2026 21:32:50 GMT  
		Size: 225.3 KB (225325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc6bb58455f631198de8b28468df6a02513dd6c58cda2c2cfbab0c94440b6c7`  
		Last Modified: Wed, 10 Jun 2026 21:32:50 GMT  
		Size: 21.9 KB (21931 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:6016d368a703e0e071ae88c8f9e79ed1f657465ac8d8dd38d620b062bfd6b324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23491503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48bfd6e0a7d649e693d1b1c51b7273929bd13ccdb0e6b7bb7c6ec15ea9fcdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:56:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 10 Jun 2026 20:56:05 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 10 Jun 2026 20:56:51 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 10 Jun 2026 20:56:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 10 Jun 2026 20:56:51 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 10 Jun 2026 20:56:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 10 Jun 2026 20:56:51 GMT
STOPSIGNAL SIGUSR1
# Wed, 10 Jun 2026 20:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:56:51 GMT
USER haproxy
# Wed, 10 Jun 2026 20:56:51 GMT
WORKDIR /var/lib/haproxy
# Wed, 10 Jun 2026 20:56:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6d3ae5749b74d7c7e5c5d59442485c42266ed6a9972e9b30b6a0aaa63b698e`  
		Last Modified: Wed, 10 Jun 2026 20:56:58 GMT  
		Size: 844.9 KB (844938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3206303dfbdfad3b1020e3c18cb438bd3943c0baf56ac4eab78f7c7c4747fb30`  
		Last Modified: Wed, 10 Jun 2026 20:56:58 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e44cfc2f754414b92a72f14617612ffbe566433393b9749f733d8e741ec464`  
		Last Modified: Wed, 10 Jun 2026 20:56:59 GMT  
		Size: 18.4 MB (18442800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706baec903f35107a6748f45b39e27bdc3371290550783d4408d7753a3b923d7`  
		Last Modified: Wed, 10 Jun 2026 20:56:58 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:d0393a9582a05f1295064c0a8d39a15eda85543bdf43aafeb09e10a4e54172de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 KB (247336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63574595465336cdc7d7b57fd584671d0ade4913cb948da717b9b325150f9f42`

```dockerfile
```

-	Layers:
	-	`sha256:76580b3996555c69b58639722c2af7aa178cfe1506efb54b861e74ae3f12eb2b`  
		Last Modified: Wed, 10 Jun 2026 20:56:58 GMT  
		Size: 225.4 KB (225361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce77dbd181aee1905dc5f41a007804f9f25ce9e02dad0c19c48506c38d024f1d`  
		Last Modified: Wed, 10 Jun 2026 20:56:58 GMT  
		Size: 22.0 KB (21975 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.24` - linux; 386

```console
$ docker pull haproxy@sha256:85f1c6bf381109b869e7ff7536822a78c3288fcff7e4f6e07606d64d90164ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22499735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600e55a8b8b1f901c29c895a2986d288d53beccd7789c10330bdf0ec6735da83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:28:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 10 Jun 2026 21:28:56 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 10 Jun 2026 21:29:55 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 10 Jun 2026 21:29:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 10 Jun 2026 21:29:55 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 10 Jun 2026 21:29:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 10 Jun 2026 21:29:55 GMT
STOPSIGNAL SIGUSR1
# Wed, 10 Jun 2026 21:29:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:29:55 GMT
USER haproxy
# Wed, 10 Jun 2026 21:29:55 GMT
WORKDIR /var/lib/haproxy
# Wed, 10 Jun 2026 21:29:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991bfc5ab3156773a870e0b8c6163fd43cf9be587af238cc5ed8f19b3b8fa49e`  
		Last Modified: Wed, 10 Jun 2026 21:30:02 GMT  
		Size: 839.1 KB (839101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938894c52f32ad973c9075e7fcc7d123ecfecc9fdd82bfa5e8d4ec1bead1582e`  
		Last Modified: Wed, 10 Jun 2026 21:30:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1abbe61996c59544afdcfc5422496571e9518bbefbc45c444377f3b4d0e73b`  
		Last Modified: Wed, 10 Jun 2026 21:30:02 GMT  
		Size: 18.0 MB (17967442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7dcafdca509f2800f001b49bdb196a4783b806ad1e444df123148139d90c7`  
		Last Modified: Wed, 10 Jun 2026 21:30:02 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:fa23a312c62556bf888b547d4192bc47fb47c2330a87e2f40177fb0996148ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 KB (247598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a5309079cf9d71a9d1264e52a32e775dfdbd0f45329f3b596ebaae233773c`

```dockerfile
```

-	Layers:
	-	`sha256:8a5f8c28a545d728d3f8553d137a1ca7f96d14af2b5e1847f3a65200a684aabe`  
		Last Modified: Wed, 10 Jun 2026 21:30:02 GMT  
		Size: 225.9 KB (225862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d4dc0b9b81b69a4c0c25e39aac93f3beb713fbf52f438b6a9bfaa6ee89a22a`  
		Last Modified: Wed, 10 Jun 2026 21:30:02 GMT  
		Size: 21.7 KB (21736 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.24` - linux; s390x

```console
$ docker pull haproxy@sha256:2e86a3b7d7e5f698855e455b70d9708cec3cb14ee0d5e859eed9d9e3b1188a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23202254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6305518a0cf22680b6f836548fee550069ceb8e91621792f2ece029685d0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:56:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 10 Jun 2026 20:56:22 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 10 Jun 2026 20:57:40 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 10 Jun 2026 20:57:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 10 Jun 2026 20:57:40 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 10 Jun 2026 20:57:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 10 Jun 2026 20:57:40 GMT
STOPSIGNAL SIGUSR1
# Wed, 10 Jun 2026 20:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:57:40 GMT
USER haproxy
# Wed, 10 Jun 2026 20:57:40 GMT
WORKDIR /var/lib/haproxy
# Wed, 10 Jun 2026 20:57:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a39d4234f28e22decd3b95018754009413840d584534f6cdf9324141bd7c67`  
		Last Modified: Wed, 10 Jun 2026 20:57:48 GMT  
		Size: 895.5 KB (895548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3233058d57ab23e58813ef7d49a319d869735543b0fe44d402d32ccb9ef811`  
		Last Modified: Wed, 10 Jun 2026 20:57:48 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb0a2513f16ce4b0aee000feeeb565b1468ec471e38c72e15ef46412610b30c`  
		Last Modified: Wed, 10 Jun 2026 20:57:52 GMT  
		Size: 18.6 MB (18575052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f24b6de3cd5351b86298cda8f3bbfe31e2a6f089f0e36ce64a99850c18ae78`  
		Last Modified: Wed, 10 Jun 2026 20:57:51 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.24` - unknown; unknown

```console
$ docker pull haproxy@sha256:0c86837d6720c92ec36239dc4cb207786729c9542d9e3683451b1a6b7eff1102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 KB (247049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394488e638fd888b80de67814c768a1f7b51b18e461ace6d97a798c58f6a1a0b`

```dockerfile
```

-	Layers:
	-	`sha256:0639baf9ad3a25cb1cec0b0ca453771a7ab7ddebd076d8919541967afaeb048b`  
		Last Modified: Wed, 10 Jun 2026 20:57:51 GMT  
		Size: 225.3 KB (225256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3dfa073e4d067a5d9dc79b8b5472b6c79003898010fce5511e5eb03e1def64f`  
		Last Modified: Wed, 10 Jun 2026 20:57:51 GMT  
		Size: 21.8 KB (21793 bytes)  
		MIME: application/vnd.in-toto+json
