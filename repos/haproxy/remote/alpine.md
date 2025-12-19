## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:28859ade669df4d04373cd14b531e07ac7ce4b81f5774ec682e2f56a02e8bc6c
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

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:b6a0e6342f3cdb86b5d680a364dde20a4c5e52a04a65ad9cacc27badeed25d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16781911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccd7eaf9f7de4f26436df22e1cdcdff2c4fb4ca8740c8bd873307f0aac32cab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 18:38:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 19 Dec 2025 18:38:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:38:38 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:38:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:38:38 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:38:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:38:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:38:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:38:38 GMT
USER haproxy
# Fri, 19 Dec 2025 18:38:38 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:38:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452370bd4034cd33cd7404b0c6cd54c5540d3b579b8998ec5bf7be4138d2ff`  
		Last Modified: Fri, 19 Dec 2025 18:38:52 GMT  
		Size: 829.6 KB (829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b8817186c75777fa2005d5b29faa6eaea47822c0ac936bac7f8dc4b660169`  
		Last Modified: Fri, 19 Dec 2025 18:38:52 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ad88670b1fe8734a57ffc74603fe47621a5f383a8b9d273656fe89708b5194`  
		Last Modified: Fri, 19 Dec 2025 18:38:53 GMT  
		Size: 12.1 MB (12090727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461fff47ae5962dd72e92da414778ee381b815514c2bf6565857554bba1d6bd8`  
		Last Modified: Fri, 19 Dec 2025 18:38:52 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b9a1105b726f49cc51708a3cb691b08cbdfbcf408ff9612313e0202a50783cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 KB (247738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b306de726fa6e21478ea19c35da4a22fc5ca230e815f62294cac8524cdb46c`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c36e6fc204a475f55290fb0cce584d23749a27c8f346b10ca410b469dc630`  
		Last Modified: Fri, 19 Dec 2025 19:58:36 GMT  
		Size: 227.3 KB (227306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2648e0eba44062bb011eb7728573621cc33ac68ab89f94e530c4de4013e1ab64`  
		Last Modified: Fri, 19 Dec 2025 19:58:37 GMT  
		Size: 20.4 KB (20432 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:5139cc110aec5bc64f62a775095b940c4eb69233102e6800fd380f5e00f3ff6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16622488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2972cf1a70b636fd6fe680b0bcf14ef2f6a13285c3c9ff7e3b863cf39967ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 18:36:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 19 Dec 2025 18:36:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:36:53 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:36:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:36:53 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:36:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:36:53 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:36:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:53 GMT
USER haproxy
# Fri, 19 Dec 2025 18:36:53 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:36:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220068911af693dc451ebb189cf0f1d784925534cf61410a73448ce65d93ade9`  
		Last Modified: Fri, 19 Dec 2025 18:37:08 GMT  
		Size: 821.8 KB (821849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90b055965cd7e5c41a441fa382b46748925135ac6849d9dd12240f8627bfdde`  
		Last Modified: Fri, 19 Dec 2025 18:37:08 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaef90995df022efa859d6c4c98ea7faccb18779997723495c66b460a06c416`  
		Last Modified: Fri, 19 Dec 2025 18:37:12 GMT  
		Size: 12.2 MB (12230772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155043d58c1ec69e2851528831cd55ac9b1369a74ef4955aaca1e509b27642b9`  
		Last Modified: Fri, 19 Dec 2025 18:37:08 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:c7ba0518d1641e5956492aa8cdfe558f962ed88b7aa8e2419d1a056fdf33c8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9373a46d9a24d228297f6850c84b080c6d4c065609b37401cb71180821e6b3`

```dockerfile
```

-	Layers:
	-	`sha256:9b5a6ee3e375ca992e394fa7bff542d7780b571290e71940f84d2c612cfe71a0`  
		Last Modified: Fri, 19 Dec 2025 19:58:40 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:c4c90d1f6fc6772e934dabefc5963d5bbe2d45cdef96d87d95e4b6c23c1ea63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16153580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbce85fd9ad98bb3e9cf7ceaa58afffe20ad0d3eade61476de3ab836dbbc27a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 18:37:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 19 Dec 2025 18:37:23 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:38:02 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:38:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:38:02 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:38:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:38:02 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:38:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:38:02 GMT
USER haproxy
# Fri, 19 Dec 2025 18:38:02 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:38:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be8a6900f856ddfb757372e40419fbf7d0e5944b478ed52fe702e4cfa038450`  
		Last Modified: Fri, 19 Dec 2025 18:38:17 GMT  
		Size: 777.7 KB (777727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9077fa7ce5305c65e9fe6be50323e51f28c2e67ca5a991c1b1a12004c7142784`  
		Last Modified: Fri, 19 Dec 2025 18:38:17 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57628b2e45fe20d00c4ae395dc4fc2f9aadd9edbeb5fc7903c1e50d29b4237b`  
		Last Modified: Fri, 19 Dec 2025 18:38:18 GMT  
		Size: 12.1 MB (12095025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c93ae94074ffd29eb7f56ea558b78bc9fdae20b52f512532536aa1445a073`  
		Last Modified: Fri, 19 Dec 2025 18:38:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:60984793b830934a028e6cbca6267921d7c9dad96ae02c4926cd1a32a06adfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 KB (247262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c998716fdb06f1a7e56b4cdafbd87dced4772c397b5702a142032e12ecccec`

```dockerfile
```

-	Layers:
	-	`sha256:590a77597b1a668ffcb78238a0fe43e371edbf42491a16cc93f3a4284fdd69bf`  
		Last Modified: Fri, 19 Dec 2025 19:58:44 GMT  
		Size: 226.7 KB (226708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c532fe1a3d2441319e8fc9b84c6ed36aca4ff871be5d2f19eb9b33269f15a492`  
		Last Modified: Fri, 19 Dec 2025 19:58:45 GMT  
		Size: 20.6 KB (20554 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:70860ebf78b2f14b9357e83599137ca9419ded21b92334ac4326621726762a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16944793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ab06b51b673268ff39caf864e0e86a9f80ed1c2f45e8be5320a23b0dc69fa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 18:37:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 19 Dec 2025 18:37:54 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:38:28 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:38:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:38:28 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:38:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:38:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:38:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:38:28 GMT
USER haproxy
# Fri, 19 Dec 2025 18:38:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:38:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04deb26a3e03395812a6c26f36bf3d5e744dc1fe2bfeb20dcf291514ef4909ae`  
		Last Modified: Fri, 19 Dec 2025 18:38:42 GMT  
		Size: 842.4 KB (842387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aeb19592f134b83730079f39cfd4ece62ec7b44c194a15ca419b936a47f34c`  
		Last Modified: Fri, 19 Dec 2025 18:38:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737d189e670acdddf0ba499ce302390b139a8ce494cf21cd62cf89f15d974eb`  
		Last Modified: Fri, 19 Dec 2025 18:38:43 GMT  
		Size: 11.9 MB (11905230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f42ae802546500700f9566585c54aa50eee3d94d142bb4e72eb42ff6b92d8b1`  
		Last Modified: Fri, 19 Dec 2025 18:38:42 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:f75fce87b3223df43a21122d01effa4368cf7e53bf52e0ca43156d56583f2843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 KB (247326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176db55659d326f5ab8a198102ce73f61092f5157d19fc2fe825aa591526d95c`

```dockerfile
```

-	Layers:
	-	`sha256:32cd698a31ee462dd64daea0eb3fb0d186aa5cf7d195cdcd419f095615e719ff`  
		Last Modified: Fri, 19 Dec 2025 19:58:48 GMT  
		Size: 226.7 KB (226736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ba3a75f49e14734a84faf44ae92a3796e9755527d88fb0e677cb2a90d8f8e5`  
		Last Modified: Fri, 19 Dec 2025 19:58:49 GMT  
		Size: 20.6 KB (20590 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:d5335399376314122bf001eefd6f449609f9b85dbab5f0628af1f4c9cf975a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16406558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cc2a3183e401540cb731cd81c9c0e242b20077e0b614a1ae79fec6cf9c620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 18:37:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 19 Dec 2025 18:37:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:37:58 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:37:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:37:58 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:37:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:37:58 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:37:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:37:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:37:58 GMT
USER haproxy
# Fri, 19 Dec 2025 18:37:58 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:37:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79695493d281eac238c3441ec97e947e1a40ceb218f68ab8310056c429779c5`  
		Last Modified: Fri, 19 Dec 2025 18:38:10 GMT  
		Size: 835.9 KB (835932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31edb209456a8c4720f0c85db0fcd65384c520e9ae05d7f0e0ab98a2a7b89116`  
		Last Modified: Fri, 19 Dec 2025 18:38:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd946beca35e7a2269063228bd65be8cc12b363eb31cfda4dcb8461f4ceed0fc`  
		Last Modified: Fri, 19 Dec 2025 18:38:13 GMT  
		Size: 11.9 MB (11883089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e942e98dcfd722c0533f4c163d69d1becee9885570377200d288dddd3518a324`  
		Last Modified: Fri, 19 Dec 2025 18:38:10 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ad3b7d1eb1541b1408164e47b03569f49193c2078ee5b1cf7765f42ea1866bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 KB (247657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835961dbf36470411629552c421b4e488fba35e98a3886d0610c0d22d100acbc`

```dockerfile
```

-	Layers:
	-	`sha256:4923b8405225890ab9eac9788765933dcf5a4123f841881f6c5ff730a6e90867`  
		Last Modified: Fri, 19 Dec 2025 19:58:52 GMT  
		Size: 227.3 KB (227271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4acf995a1fc6bf1dc0fae0ffd9af1fd963a85ed2820d789936fe48401d7e45cd`  
		Last Modified: Fri, 19 Dec 2025 19:58:53 GMT  
		Size: 20.4 KB (20386 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:ae2f498c609c046ed5416543c301d3a66d9467ecb0cde2821e97dcac87b0ecf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17519321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3551a03c5e0289a138d94b042b16c15f76497544022d8a9b2e8f588b25ca1917`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:27:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:36:06 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:36:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:36:06 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:36:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:36:06 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:36:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:06 GMT
USER haproxy
# Fri, 19 Dec 2025 18:36:06 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:36:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a0fdc4bb301c69fecfecf50058cde63750c19fa0b3a70fa341b6f2fcf528f`  
		Last Modified: Thu, 18 Dec 2025 00:28:33 GMT  
		Size: 865.8 KB (865810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00141f74db030864fe82dfb8884aeee311a70a3e2d18b678d14d71fcb989fdad`  
		Last Modified: Thu, 18 Dec 2025 00:28:33 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e2f975a0f760bb2a9a707df6eb6449a45e9d8ce7b9fd291669f995123f6b23`  
		Last Modified: Fri, 19 Dec 2025 18:36:33 GMT  
		Size: 12.8 MB (12824316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f123ec14720d3b72beeaab6828740896914032b261cd343cdb19ba4c3ab5cc`  
		Last Modified: Fri, 19 Dec 2025 18:36:32 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:fb284193741e7acfc68bff11385ab3e1ca29ca58ccf6c2fd04e8b230456d092e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebf887a1450acbd8f224e9712d458ab3fd956fd5d54c60aa8b4086e23852d81`

```dockerfile
```

-	Layers:
	-	`sha256:d38128d42b8dac0492e8168f38f0eef76e15b8edb7e2dddbbc402daaabd13fde`  
		Last Modified: Fri, 19 Dec 2025 19:58:56 GMT  
		Size: 226.7 KB (226701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02cd580f9895b79b5bb98d91974c8698857a0c64322818cbb6a0b247212b7da`  
		Last Modified: Fri, 19 Dec 2025 19:58:57 GMT  
		Size: 20.5 KB (20492 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:733fa9545d05d0aafaae6c4bc6edf1202c0ea915aacb58c1cf84a04b5ba3526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17532996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e676d01adaa941845f66be80d69bc858119f1ee9a85a699d18b4a6299d26349b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 05:00:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 05:00:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 05:29:34 GMT
ENV HAPROXY_VERSION=3.3.0
# Thu, 18 Dec 2025 05:29:34 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Thu, 18 Dec 2025 05:29:34 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Thu, 18 Dec 2025 05:29:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 05:29:34 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 05:29:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 05:29:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 05:29:34 GMT
USER haproxy
# Thu, 18 Dec 2025 05:29:34 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 05:29:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac202a4ea053c559abb0839547921026b5c60ef3268d982da82c523fc6ec02b5`  
		Last Modified: Thu, 18 Dec 2025 05:15:11 GMT  
		Size: 849.9 KB (849928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2942b29757a2f3be1a51fbe0d838f5da7e1811a07e28b7e01723666deab1f454`  
		Last Modified: Thu, 18 Dec 2025 05:15:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f2feee933bb54dae5a97150fdeca1ac47a903922d5aa5084f75ec51bfc5660`  
		Last Modified: Thu, 18 Dec 2025 05:30:25 GMT  
		Size: 13.1 MB (13097685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eb4a0ce493f30b92870ae4283954e73fd7dc9644da0cc48b9d84165a551120`  
		Last Modified: Thu, 18 Dec 2025 05:30:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:872b44c7e7e66b33d471bc069c5f37ec31a40e5958d2aa7c2bf42ffe428d6233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb1bffb865620d460dca176e0ba8ac909f77f94e87d7b88fb1955c53556dc7f`

```dockerfile
```

-	Layers:
	-	`sha256:158f0895e288c5b0857af1bf686ae5877ce5f592e9ed2563e57510c23017e11a`  
		Last Modified: Thu, 18 Dec 2025 07:57:18 GMT  
		Size: 226.7 KB (226697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1804366d399071d4907f90ea992223c374f88051e7d68101d0896f3fed7264d0`  
		Last Modified: Thu, 18 Dec 2025 07:57:19 GMT  
		Size: 20.5 KB (20491 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:7fec31df62241a683fe11caf015a8255e48873afd38862806f37bd371f20d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17084023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fcce3c2c243a327f58d7bec22321a016825d9c8b324088191c2cf7b2ce0cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:26:19 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:36:36 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:36:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:36:36 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:36:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:36:36 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:36:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:36 GMT
USER haproxy
# Fri, 19 Dec 2025 18:36:36 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:36:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb4c31af08adac97c43e9de41558d8e4f045415ddcc149f4c0c086792d3713`  
		Last Modified: Thu, 18 Dec 2025 00:27:34 GMT  
		Size: 891.5 KB (891548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0a83fd7ffdb53f0a260c4043ad39b2781b388b81d8b97ddf6b144b89af86`  
		Last Modified: Thu, 18 Dec 2025 00:27:32 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0c834bf89bf4c4dc73b403e7c8b6a506739dc93cb04752d2f5699eb6c87410`  
		Last Modified: Fri, 19 Dec 2025 18:36:52 GMT  
		Size: 12.5 MB (12466730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df76f005c5e11f41559fd629944c963e26954d3144396d20bb82b68f6c6ae81`  
		Last Modified: Fri, 19 Dec 2025 18:36:51 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:8134199c9de32e40eef8f089876345df4512d8a723d80bbe271d52e7495d3431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 KB (247087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76903db423e902ddbba4b6746fa501028d52558ad54e81230c537ebf258b10e2`

```dockerfile
```

-	Layers:
	-	`sha256:73a50c09c663b113e5fafc0923f2e7ef09579561b1920df1e25f44626a4cee17`  
		Last Modified: Fri, 19 Dec 2025 19:59:03 GMT  
		Size: 226.7 KB (226655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781e0845bdcf74d8f5aba32c62a7bfdde5c9b8c53cf7e03de8928dd35a85f958`  
		Last Modified: Fri, 19 Dec 2025 19:59:04 GMT  
		Size: 20.4 KB (20432 bytes)  
		MIME: application/vnd.in-toto+json
