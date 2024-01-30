## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:8a1f01030f4f3898a9edccdc3f7aac259cdb9c05947d8c42b0e13feaaaa26356
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

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:a350629bacb1f33401f2a6b89fbee18782ad21c26ef7436b2b2c578bca6f92ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11927076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5be38997c40c03e3e6f691d36ffd1bcb7c32c9d4847e96d42c54de05af5606d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c180cb712a5e81c8f2fe4fa08f0f1b5bf890943720d62f5438b29942034143bb`  
		Last Modified: Sat, 27 Jan 2024 00:53:35 GMT  
		Size: 284.1 KB (284100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7c764571587e1c7ffacb78d22e82c41db0479c0b0b222f55e02eabe84d3f6f`  
		Last Modified: Sat, 27 Jan 2024 00:53:35 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4224470ad24a360eef8020d68e1df41c5607fce302c95845a225f14ea2aca3f`  
		Last Modified: Sat, 27 Jan 2024 00:53:36 GMT  
		Size: 8.2 MB (8232512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de124e84d23960af2d57207a7fce0cdfd145f4a3dafd92b5fb348509ea667d`  
		Last Modified: Sat, 27 Jan 2024 00:53:35 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ecf0e8d1bd83c0a443c23bd871c8770f4daece1878971eb37265714694ec75c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 KB (172122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0653438f3f56b40a46a2489c4d4111ddce7fffea9878f017697c1a7e9036b6`

```dockerfile
```

-	Layers:
	-	`sha256:eb88ac35c67cf3bec4eea332faacc270dcecfab966252086252a2507fc733439`  
		Last Modified: Sat, 27 Jan 2024 00:53:35 GMT  
		Size: 151.8 KB (151763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ea90d54feb15fc4b4c8a676cb3c817fdff61c185c9cd5a779182fb2a209efa`  
		Last Modified: Sat, 27 Jan 2024 00:53:35 GMT  
		Size: 20.4 KB (20359 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

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

### `haproxy:lts-alpine` - unknown; unknown

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

### `haproxy:lts-alpine` - linux; arm variant v7

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

### `haproxy:lts-alpine` - unknown; unknown

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

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3e529b3622d35ad1243111c450edbed703493a5fa66a0e8f2466e6b4688cf822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11822563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2407dec963511cbdca7a7312ffd798c18f51abde81bdfbbb06c80bac5fbf9648`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf48479048bb565d382f52bdb85bda76f60fc7ed30d73e1b86bae9c4c095177`  
		Last Modified: Sat, 27 Jan 2024 20:20:31 GMT  
		Size: 286.4 KB (286380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5766b2c000a898c877dd388298f28066de999033d4a9cbe97368928217e5575b`  
		Last Modified: Sat, 27 Jan 2024 20:20:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e32c0ac502b5bebf4491d8a6f6624f89aecffc48b4c488e01fb6a15c13c5d`  
		Last Modified: Sat, 27 Jan 2024 20:21:59 GMT  
		Size: 8.2 MB (8186735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594e39e16d2b06d97c296dea71e52290216c8796967e863e01e9d44846efb648`  
		Last Modified: Sat, 27 Jan 2024 20:21:59 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:421422f8f25449a93040bd4dd414cbb22ca9009cd3e6f1912884c19eed12417b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 KB (171985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9547145b2adf68808bbf136d31823b8a8b5ecf5c9ce00689e128e323e34b415`

```dockerfile
```

-	Layers:
	-	`sha256:9030723e63761ff8232f9bc9bd0e8f87c4e6e78b7041b64ce6d4725cea6c58cf`  
		Last Modified: Sat, 27 Jan 2024 20:21:59 GMT  
		Size: 151.8 KB (151778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02cfd32b49ea8e625f06c31408532990f13e331dfc122005622f84709d9f9a80`  
		Last Modified: Sat, 27 Jan 2024 20:21:58 GMT  
		Size: 20.2 KB (20207 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:a3f0175ddc20e6fcdf50fe398798e60d1635e3f753fb3c6b9c1d87f58aecf607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11565570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98734a6a0fcc3aafd51f120d4870468a3e24a3924fb51ccdb76afc7d0295782`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a96d422cc901102fea2ff0eff1aa41679479c038744a718f60027035a73ad18`  
		Last Modified: Sat, 27 Jan 2024 01:54:33 GMT  
		Size: 284.6 KB (284553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114644e4f4ffcd156f1b9c4f9c4f6caae018f6e8d577527caee81ed1ecf0c17c`  
		Last Modified: Sat, 27 Jan 2024 01:54:33 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a013e41a274dcfa1146449a6bd3e643d618b786f20a28959d991f409686e382`  
		Last Modified: Sat, 27 Jan 2024 01:54:33 GMT  
		Size: 8.0 MB (8035196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a15648601e990e17d9cb9d26e2b79695d34a08aa2aee8bb5d37e1af0bda4e7e`  
		Last Modified: Sat, 27 Jan 2024 01:54:33 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:888256f29b966c26dceb6d336871e9486a6d3c39e6d7214851f895c6e8430018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 KB (172044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a15911303d3aa2830308c7f11a65eb9947e0be4d487c0a482054052a3b98c20`

```dockerfile
```

-	Layers:
	-	`sha256:01d74dc84209df17fbfed7d55fe8ccda3b633825a4fbd5ee08d73d35fa630ad9`  
		Last Modified: Sat, 27 Jan 2024 01:54:33 GMT  
		Size: 151.7 KB (151728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9d2abe7909bf76fd378cebca6d79f95e09abeae99056ef34408d35ecb3ec84`  
		Last Modified: Sat, 27 Jan 2024 01:54:33 GMT  
		Size: 20.3 KB (20316 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a3525a4cc479d420fc28d60f494b529cae09cd41dcd2e866f496866fa89972db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12252168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabed510345988c9fefea1f2419ba72cf1bc291ca90253f40b40dc45a6089177`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aebe81c4e89f4c7254ed8fb6768a3c4f37adac300fa56e42cb95c4f441d6ff`  
		Last Modified: Sat, 27 Jan 2024 09:38:25 GMT  
		Size: 286.8 KB (286764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cef88ee724bdac7ce4f8d742e2fea62c85256324c691b8506d665190de35a4`  
		Last Modified: Sat, 27 Jan 2024 09:38:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4678d3fcf476bd1494b5ade659e693ba8c764f8e61d537cb4a0a42b727e543f`  
		Last Modified: Sat, 27 Jan 2024 09:40:03 GMT  
		Size: 8.6 MB (8605317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d11db9c69e14b322589aacefcc6f01c6c6f588f2e07affef4d69c6610bc034a`  
		Last Modified: Sat, 27 Jan 2024 09:40:03 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:26e59d1452d89c5d482e47230f4f3a68f3ae8fdb45595a485bbbe0113eb174e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 KB (170420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823d37d09868c44e02b1cb60f2060e52ee32f8db23a0518683c18f7321d80221`

```dockerfile
```

-	Layers:
	-	`sha256:c393f6059c090de393007890f4b842e97353d214ea51e7dba066c5011f0e6811`  
		Last Modified: Sat, 27 Jan 2024 09:40:03 GMT  
		Size: 150.2 KB (150173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a480eff276991b0ed92f10e7a75ab60d85d503279a23c334767e6e40b9c57ed8`  
		Last Modified: Sat, 27 Jan 2024 09:40:02 GMT  
		Size: 20.2 KB (20247 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

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

### `haproxy:lts-alpine` - unknown; unknown

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
