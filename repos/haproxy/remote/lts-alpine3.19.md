## `haproxy:lts-alpine3.19`

```console
$ docker pull haproxy@sha256:d6d514aad6d187a76bac6f7f43480535e5092c0702d356bc7d733002c7bdea02
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

### `haproxy:lts-alpine3.19` - linux; amd64

```console
$ docker pull haproxy@sha256:a435f6659bd06d4950bb6867ba22cf02f78c2e0a510262f5d3d3a4307e2b6ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11930186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193755fd5ea157d61ba54f7d468487299a591c917e053cbeb619bc9f65cad38a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_VERSION=2.8.6
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.6.tar.gz
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_SHA256=9fd034368be66880bd86a300c13dc03bc13521ee2654880dddf192785aa28d51
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 15 Feb 2024 18:13:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
USER haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e073778d48dd9952a218572b21fa05d60db1741ada51bbb7757dcbfd8ab39`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 284.1 KB (284105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c68a64edb5e88f8201a258b7007dc107b271b5da384c052317b7cc3c3aae798`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46055b087625f996295990f6e0bb4c16a7e4b02d9346689aafb432720796b1ae`  
		Last Modified: Fri, 16 Feb 2024 19:51:48 GMT  
		Size: 8.2 MB (8235616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7158bc5aa863e2af29e5b913a43514a09163f213d63447fb164ae46b098996f`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:e959f8ec8d1f6c8142eebf6825fa6b8d9453e575251ae6e70419d74650d59826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf69da0c2ff2d3387787f889ae2b1fa966d2ff93689d865882c097faeea9b97e`

```dockerfile
```

-	Layers:
	-	`sha256:8004513ce0060136c490bbf8982885ea263afb806b1c72fae6fec4e6c1045215`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 175.9 KB (175931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab097315a80636a0255c0866831f8e941dbc23fa7d09e76c983397c88e0f13a`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 20.4 KB (20359 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:413424643d5fae84b701138927166373d69a20c707138e8e7f4e30904824ffb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11531291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbd74caf4e96008f2e2da47cc49aee869fc4649bc4eda68a5cd709ec5af82d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a906c346c86052dfda1a0ac5ace55591e353dede0bded54868e3832931d620b`  
		Last Modified: Tue, 30 Jan 2024 05:43:17 GMT  
		Size: 285.0 KB (284963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bee20f36a71c7a1f806023f26e79cd1cec38015023e9682fba124b928aa9b1`  
		Last Modified: Tue, 30 Jan 2024 05:43:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba514adbda6d74f1d40e15c5eca2f6edce08ba52c35d0c5d15ea5a24fe7ef466`  
		Last Modified: Tue, 30 Jan 2024 08:50:06 GMT  
		Size: 8.1 MB (8079198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484eee735e1f7b6f593437d332b2855687e019f6e0222d27b963eb6f86464e16`  
		Last Modified: Tue, 30 Jan 2024 08:50:05 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:12534b414840d5a62c144bda7b1b68870d001b8ac1402c79badbcb9b86256ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c88821dd96d494232161ba2241c246c0f3ad62b1c4fda5987f6a42070a436c`

```dockerfile
```

-	Layers:
	-	`sha256:23c842c2f4e17a65dcba6a1f5914c1d3b677b070040872e4efde57c220df47b9`  
		Last Modified: Tue, 30 Jan 2024 08:50:05 GMT  
		Size: 20.1 KB (20090 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:32e8d86ff901ee89eb67fcf3166f2fe8449acb5beeb450a08d2fd6bb0355d386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11162103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c79c764d804435e28e259b30c1c85470229cc750bd24c54a77a1556789be54d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88b5a1df344dba015a48cf517cd65b7d944059948785272c0f86f160c45cfaa`  
		Last Modified: Sat, 27 Jan 2024 15:39:20 GMT  
		Size: 284.1 KB (284131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d44c6bcea807b5f61db6d98461f4f7bf5ddc617c1946216a8cbf55c43a9cb12`  
		Last Modified: Sat, 27 Jan 2024 15:39:20 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf62400c883496f8811d279cf126afe6ecb94eb7509a5069109a7118ff6a23b3`  
		Last Modified: Sat, 27 Jan 2024 15:41:47 GMT  
		Size: 8.0 MB (7957337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88c3a24175b23ccdd9b1f65e019f2293a11d24b4e5f9dfd14f8287dc24a499d`  
		Last Modified: Sat, 27 Jan 2024 15:41:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:dde9142744e3d0222e41b1eb1df9b012676f024a5f249858c00d6b30d0b1d5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c4407cb61371341b7be772ef450b2b776b9c24ac28214427e3e099c22963fd`

```dockerfile
```

-	Layers:
	-	`sha256:e5cf4aa2c451344005ff800968ae6498fa8702a8d4beaf06adc9e94236f0a4d4`  
		Last Modified: Sat, 27 Jan 2024 15:41:47 GMT  
		Size: 151.8 KB (151815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be849b718f1743e0267e3493fb8581cd698292b7e673ffbf9150c518830afa38`  
		Last Modified: Sat, 27 Jan 2024 15:41:46 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9d67b96fb78d3ae7110c75b5b4dd9315ec7564a657b43a1b04c7188070f50c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11827395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc23ff5e302da7fc790908d4a5b521f6823a0cd533454d595e119d2cef0eafed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_VERSION=2.8.6
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.6.tar.gz
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_SHA256=9fd034368be66880bd86a300c13dc03bc13521ee2654880dddf192785aa28d51
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 15 Feb 2024 18:13:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
USER haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffdba998a7d9cb80d56d3a75f4823cbc595ce14eb785a35376c8d2f7f48855d`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 286.4 KB (286386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d642c0f21728d496d6aa268bd2d344d9e3c63786f31cd6e353da1abea11b47ed`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02718f4a22957dd091089936cdf3a806764208ec6878fd61cb656b460237d8d0`  
		Last Modified: Fri, 16 Feb 2024 21:06:40 GMT  
		Size: 8.2 MB (8191562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a4e734c955116bc216b62b1823f545e9a7a3dddd822ae68e31a681c7421e58`  
		Last Modified: Fri, 16 Feb 2024 21:06:40 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:467c36f41ab133466a1b0c13200e84d6ed622191ac88ca10d9fccc2e6b80ac3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 KB (196153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40b8ad50de7011c750e74e91b6def15a945e3eb64fc138b58956be6a0683ab4`

```dockerfile
```

-	Layers:
	-	`sha256:8c5bb091b104320be61aa675d333d88600057aae338b45820d35f0894c6f2013`  
		Last Modified: Fri, 16 Feb 2024 21:06:40 GMT  
		Size: 175.9 KB (175946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc14e10510e16d3e064e58207722a6159b4eee065737a3d5dc26a6ce08d1291`  
		Last Modified: Fri, 16 Feb 2024 21:06:40 GMT  
		Size: 20.2 KB (20207 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; 386

```console
$ docker pull haproxy@sha256:720b1107bed9e46447024867c1bef5cdca4d65b2bb16c540a121dea28ec7ad44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11573059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68df768a4da0a15f8d4696b7c58ba2a6ae4699cba8a60e27a16c76d84bb77010`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_VERSION=2.8.6
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.6.tar.gz
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_SHA256=9fd034368be66880bd86a300c13dc03bc13521ee2654880dddf192785aa28d51
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 15 Feb 2024 18:13:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
USER haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4339332a94fc3066c6443ee3f1448affc44c5f0da8c082624f3f54a646145af3`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 284.6 KB (284560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b9e3e8a2f00ea52c479c1906648ed3eb2e7a2a44453c69534bdc61592ef1e5`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab46e1314981458453941ef818c248217e06c89a0442ba673658885f02d1c0c`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 8.0 MB (8042675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7158bc5aa863e2af29e5b913a43514a09163f213d63447fb164ae46b098996f`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:a9441b91db23feb778a3dea1c576a1799c430dbc96baa02f85c9dcc3497caf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 KB (196211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba13ed54cfca6de655e89daa5df01c24470ae8a12b87e4f854014faa372cc0e`

```dockerfile
```

-	Layers:
	-	`sha256:ea0d203b39d439f3de8e6b5c258bf9caea9a532e566974590716863c56cf7cc4`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 175.9 KB (175896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:516a11cf7064f39e0e46961eacc729163f9d7da5f79e8a9ec94655a9e1749540`  
		Last Modified: Fri, 16 Feb 2024 19:51:47 GMT  
		Size: 20.3 KB (20315 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; ppc64le

```console
$ docker pull haproxy@sha256:570b10608a09a9b7e8b186e5eaf8b6310b0bfa86ad02e5a41441849b24301854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12324531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473b03e17a737dda6793c9c50dfd625146fb95d6b6cf12cbbbaa6cab0b1d8779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_VERSION=2.8.6
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.6.tar.gz
# Thu, 15 Feb 2024 18:13:25 GMT
ENV HAPROXY_SHA256=9fd034368be66880bd86a300c13dc03bc13521ee2654880dddf192785aa28d51
# Thu, 15 Feb 2024 18:13:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 15 Feb 2024 18:13:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 18:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 18:13:25 GMT
USER haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 15 Feb 2024 18:13:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562ebb05af8ae069f087bcc9e91a066e4f2b4cac2721a591b77d7fcc503aa75`  
		Last Modified: Mon, 12 Feb 2024 22:41:20 GMT  
		Size: 286.8 KB (286751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d6fcf4017a80ca60bfd78b795af26fae6f2291641f6c9f6f5451f0e6a5dcd`  
		Last Modified: Mon, 12 Feb 2024 22:41:20 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e108059345d4cfe81f891b56150fc6dbc8d7a3309e79f0d68a1fc94491fc9`  
		Last Modified: Fri, 16 Feb 2024 20:14:43 GMT  
		Size: 8.7 MB (8677692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95d1b0013f8cebec2bea960171863d1f894ce7555112b4986d2bd654f55c1`  
		Last Modified: Fri, 16 Feb 2024 20:14:42 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:3e2dc3dcac45d04ce166886746893d01247e6691e9e4a4371a979d0c1faa7854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5738d36133e9ff1109999e48556703f565ad7acd53c0a5835717a6b842d99e`

```dockerfile
```

-	Layers:
	-	`sha256:3d11a77456532839f834f7a44b8000385d5acf85127557d5f56013aa6aef0e3d`  
		Last Modified: Fri, 16 Feb 2024 20:14:42 GMT  
		Size: 174.0 KB (174023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d072628e1a5aecdf6f7e6cfd6a68e7fca638376edb6b404d24176bf3d027f11`  
		Last Modified: Fri, 16 Feb 2024 20:14:42 GMT  
		Size: 20.2 KB (20247 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; s390x

```console
$ docker pull haproxy@sha256:18209046da185b099fe7eb1c5e6fc5a7f93b79d315317257701500a230f54c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11924508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216e3e31351fb9f7135b8291542689719b769c35e056216d0234807211ace5a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35065c1af70729689007d4a8937de5c3c422f8a4752673f9a014c1b0442b94f`  
		Last Modified: Sun, 28 Jan 2024 07:22:08 GMT  
		Size: 285.1 KB (285098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33731b789b7e727202c90f8661ab8d0fc2ec15106764b2e97a75cddc289f4940`  
		Last Modified: Sun, 28 Jan 2024 07:22:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4215731a3271cf67b084e79a4c9db5fcf66007a11705f4b8f0b45a701ff04f`  
		Last Modified: Sun, 28 Jan 2024 07:28:59 GMT  
		Size: 8.4 MB (8395039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccfc60684d441439c89c6cbbca7ada739cbc31781aab27ec8ef64652ea5b1d`  
		Last Modified: Sun, 28 Jan 2024 07:28:59 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:1b7e59bb4e3f03993c5dbf0fd0e495365681e5be8cd50998e8c703bad0bf5537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 KB (170320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeefd10923c847aea7a6c17cee9446dc47d319a433598bc3ebaecc3070bc76f`

```dockerfile
```

-	Layers:
	-	`sha256:3d14b5205c29d4bf2b17951688084b87d068386e3acf21b2affc2b8514a7e9af`  
		Last Modified: Sun, 28 Jan 2024 07:28:58 GMT  
		Size: 150.1 KB (150127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e41a5a8440516de3d0741a58541236cd4acb824c7c933a40922f4cc9be4384c`  
		Last Modified: Sun, 28 Jan 2024 07:28:58 GMT  
		Size: 20.2 KB (20193 bytes)  
		MIME: application/vnd.in-toto+json
