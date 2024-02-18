## `haproxy:lts-alpine3.19`

```console
$ docker pull haproxy@sha256:702ca3f73e2e39fef0060347aaaa453107a8a66664b7aa642f876927d4ad7377
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
$ docker pull haproxy@sha256:80c66e9f8ddb6747bd8d503e1fecdf4ef9638d04c9b336f7a4c7cfa79c7db6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11643370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ea33ea00049296f9ff008a6a18e0ee831bf6a2e4bc1436868766821a0c5499`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85b233432e251d0de4abe1b2c20dfe2d45ec02e9a7a8538ee8eebe26145977`  
		Last Modified: Mon, 12 Feb 2024 22:13:36 GMT  
		Size: 285.0 KB (284969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975d9dcc5ea16ab012a0d6d906197cad7511267e73bba790ac96568a5b4f948`  
		Last Modified: Mon, 12 Feb 2024 22:13:35 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787f311142b1153814a6c0400533036e20617d504b6e95ca51ca96eeb665ea2`  
		Last Modified: Sat, 17 Feb 2024 07:29:26 GMT  
		Size: 8.2 MB (8191268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6744318e1f159e5c080c43196bd4a3d72b9c02b2bae1efceb54735d101c112f`  
		Last Modified: Sat, 17 Feb 2024 07:29:25 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:00abe3144828e4d53f47587f1a62e0131ecc5949f4b66a3069e92703029ed14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1defc5f39f1707b3ece9d39dd898d47bf2f29f7f8156fc433e66baaa06c2289b`

```dockerfile
```

-	Layers:
	-	`sha256:3803eef6b39d38dd2fee7552bb06cd6d84733e021f7aa404fc3b358247a7bca1`  
		Last Modified: Sat, 17 Feb 2024 07:29:25 GMT  
		Size: 20.1 KB (20088 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.19` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b4747ed904bc83918c09e8dc26c8b0335ee0715e77c342460bdb4fa15709b000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11272309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfa05112175e6980fc84ee283bf8630a891375c5f983156241fdbee780e68bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
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
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34457f305359ab30eac9a9890df125c672c840e6448eec07d80321c3bac0a29`  
		Last Modified: Sat, 03 Feb 2024 09:41:43 GMT  
		Size: 284.1 KB (284127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f278677e1da6524e7094dc917e821adc1a7434e6a442d28872bbf23b4304f`  
		Last Modified: Sat, 03 Feb 2024 09:41:42 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673a77d1f2dbd2816d23086f7a66cd8625cf8b971424b3a83224bb0f7a61ee94`  
		Last Modified: Sat, 17 Feb 2024 07:25:29 GMT  
		Size: 8.1 MB (8067552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cab1a7664371b5f4a7fdb5544dc86ab173f56d1f906154530148a13d093355`  
		Last Modified: Sat, 17 Feb 2024 07:25:26 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:c409e8e5db2d471196a420221262f8d7f8317d81a039ab75869eed35d703730f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e069e470d6a7c96e040b1c9b15ce24ec14c0628443c73fe14b750db7882f300`

```dockerfile
```

-	Layers:
	-	`sha256:9cb5316d113187207f260021421f2225ab5d59bcc93c12a95c9a6c1f63f81123`  
		Last Modified: Sat, 17 Feb 2024 07:25:26 GMT  
		Size: 176.0 KB (175983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af8e76c6611bea74e7de752499d2b07ba33b3569ff0878ea753740364a4ca30`  
		Last Modified: Sat, 17 Feb 2024 07:25:26 GMT  
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
$ docker pull haproxy@sha256:c70a1c1808a451ba0c88a9d9fd0882cd412caf86a37a1ed0e51a68e91a3460a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11951297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c886c70c4897ba28b0ef51fdac7ea04aa34f3313893a7feccb71916348d384f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62165fa6c8db49ded3bb26d6fb91f158b9c77eaf2bf8de692b2da00a4f72dd48`  
		Last Modified: Tue, 13 Feb 2024 20:16:10 GMT  
		Size: 285.1 KB (285098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf97c2ae52a60b1d36228750242f3ca9e590b00fec1eeb6212ecc1f2deba11`  
		Last Modified: Tue, 13 Feb 2024 20:16:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfb3b06064ddd23b033e420dc0727b3c590317b58c5012a9aefd6520026eca1`  
		Last Modified: Sat, 17 Feb 2024 06:34:59 GMT  
		Size: 8.4 MB (8421828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a0d55c7c4561eddce53c31d35eae9e3597811d2ca72a746bcbc9470248d386`  
		Last Modified: Sat, 17 Feb 2024 06:34:59 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:aaf60f70de58244e08dd1bc984ebebdd320295d749e4ff5a77dc3fae57e66c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e00737250a66ef45a732d16de22442676aa92c4eeb6db7ebe8309ad759cfb07`

```dockerfile
```

-	Layers:
	-	`sha256:d8ebb4d686559261efdf4181b12789f811a2e3b4c62347ec0adced7ab530ea11`  
		Last Modified: Sat, 17 Feb 2024 06:34:59 GMT  
		Size: 174.0 KB (173977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6811e67341f16b50ba73975992891ced0ff0858d6cbde87beabda8f8e98c3c82`  
		Last Modified: Sat, 17 Feb 2024 06:35:00 GMT  
		Size: 20.2 KB (20193 bytes)  
		MIME: application/vnd.in-toto+json
