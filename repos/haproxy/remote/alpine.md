## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:7d1d22e296b3fde04bca684206bd83ccec1db3ee446f8d65d38bb0a87260cde7
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
$ docker pull haproxy@sha256:b82ec48ab01543969a82b9644b140a1a6562dd5caf5741ee2a1c90dbc3806e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13118452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1bc2abea9542a22fd80e9644195616aa458deb0d761e0319f29da7e75fdd46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Jun 2024 16:50:59 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d482bdba40b18a626737ff4444c378dbfa738ca80648415edba6fa89ea32e10`  
		Last Modified: Thu, 20 Jun 2024 20:55:46 GMT  
		Size: 292.4 KB (292427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12956b4e071d4cde9aae9b24ff7d5c3ea9adb645508d8422112d9d02226f1108`  
		Last Modified: Thu, 20 Jun 2024 20:55:46 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f5c385a58491dcc6901fce0a40e9f1a404f75ee0f028e30e49fcdcdc83829b`  
		Last Modified: Thu, 20 Jun 2024 20:55:46 GMT  
		Size: 9.2 MB (9200729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5cd435034112f6e4ec5fca627d694d8031026f1d3ce278b7dc76ebe0f5bbec`  
		Last Modified: Thu, 20 Jun 2024 20:55:46 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:43e98aef029589ff77b57ae224ab0191632de500b483c60f18bb6515565b87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 KB (197468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef255f4acd2c074ec48f2df2a85661f88cf553a29b54124d590df856eed0d2`

```dockerfile
```

-	Layers:
	-	`sha256:1d5ff00d722085bc33ee8fff85c9aa6554a7cb3962a21648c2bda4f1031769cf`  
		Last Modified: Thu, 20 Jun 2024 20:55:46 GMT  
		Size: 176.6 KB (176618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f582c224165fe32747b8ed855218f8566f872adf9095c2becc8ed0f1c791538`  
		Last Modified: Thu, 20 Jun 2024 20:55:46 GMT  
		Size: 20.9 KB (20850 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:e7ac87c49a30a160294beefa1081413ca6aa40bac35f73d5a65d231c08719159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488a821c3992446014a865db2bb7a2b6bd2d4402a5c3ac2730484ee586288495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc31ac07d597026cfe0f6aafe7ffde8bdd264dbb85751d1553ae91fd4184100`  
		Last Modified: Fri, 14 Jun 2024 20:08:31 GMT  
		Size: 293.6 KB (293623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8125a377100d4acacbf10c8e340a06b758da03d3862c963047e7b8007dd21e`  
		Last Modified: Fri, 14 Jun 2024 20:08:30 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be8cb89e678875f121cca1aa41affc426be882ca377a98ab5924b0b3c4daca`  
		Last Modified: Fri, 14 Jun 2024 20:09:21 GMT  
		Size: 11.3 MB (11286766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05177e64897e4cff22392199084369c8add1b02be97c7adadfd3e7d74456675f`  
		Last Modified: Fri, 14 Jun 2024 20:09:20 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:eb0e84c713f7816d6000d553a0bcfb908f3ee81617855fc65486472f723d8f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97e35308cd4460e87e35552f7665518dc1bb21aaf4b16ced8df409945b51b23`

```dockerfile
```

-	Layers:
	-	`sha256:365b3ce61e0761de4e1ce77e2e69f0e2ea6e46f927444e8a8967cb934fdd2102`  
		Last Modified: Fri, 14 Jun 2024 20:09:20 GMT  
		Size: 20.8 KB (20762 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:15ecf7a60c3cebfb2d5d5e5eb3d5e39a2c0df9638f5a860da29c1d71303b4e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14377962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61ff54f35cc799b0e31ec154f48a59d417280bde77721eb36d9641df1f4855`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
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
	-	`sha256:4b7483e1177212f1d505509ce24567d8c1061f6905ea3633c107400054ebe01f`  
		Last Modified: Fri, 14 Jun 2024 20:22:32 GMT  
		Size: 11.0 MB (10990008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2921de531c052937f5d35fd2c5092ea658ae843ea8e45b52946f8004524e3e4c`  
		Last Modified: Fri, 14 Jun 2024 20:22:32 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:37d589a19f2ffd774a97b8871c837941ecce63ee93d841ddec8719cba92859d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 KB (197665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e83b8a8ba4162121a47395a622d85f51e02180d478e9fbde49f9fe8b4a8e12`

```dockerfile
```

-	Layers:
	-	`sha256:1a9727ef5ece5bcb9aa20cafe3aa97e593e04e268afc63281499d88e3b502de9`  
		Last Modified: Fri, 14 Jun 2024 20:22:31 GMT  
		Size: 176.7 KB (176685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd422a4acd494d650ca7ad48eb9fa7b3e3f910f607d8649741c1aeb4c97026b`  
		Last Modified: Fri, 14 Jun 2024 20:22:31 GMT  
		Size: 21.0 KB (20980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fcac1e352e14e165c0e38e3ade87153803bc91b4742dfe6303322ea0d69ece63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16413744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da1f875e8388c0ac28ecd782017c1868d4b0df0971fbc11c99e3951d7e30cba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
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
	-	`sha256:63970ec3df7c5923fd466181ecac3b3a1e2c9fa76b591bb37ee0a871172c3b55`  
		Last Modified: Fri, 14 Jun 2024 19:55:24 GMT  
		Size: 12.0 MB (12030060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3edef6cf9ada4092be3cf0b2e5f622b05bda338d2afb984cdbedb3fc6c2f802`  
		Last Modified: Fri, 14 Jun 2024 19:55:23 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:95e85e2b587f07954b0b7c9e47a1889742b5fbdb0647aa84303a1551ba5d36bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2fdeae8d59203e9d18d9dae7da071cfba2b930b0669b85363a01b91b466326`

```dockerfile
```

-	Layers:
	-	`sha256:525ed1063babfd0dc1b92bbfaf7f919bc5fdbf221df79402eff49d278c52b094`  
		Last Modified: Fri, 14 Jun 2024 19:55:23 GMT  
		Size: 176.7 KB (176721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38be7ec78cd33c0c0a697d92dfa9e02da22373826bfa7c65a6e2983838c1417f`  
		Last Modified: Fri, 14 Jun 2024 19:55:23 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:ffd1c053bf9e66a10bd071c564390e346187e94ddd080a193852e6ab92e2c8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12760918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6bad862826499a624c7f2aebcb0ff2272b7f0a57806841f1d307bab373826d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Jun 2024 16:50:59 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6804f78f737c22625be803df1c9428ab2353ed2904268706c5926f44329ffc`  
		Last Modified: Thu, 20 Jun 2024 18:54:27 GMT  
		Size: 292.9 KB (292888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19abe84cc2c75e123003d990bf7b91f14396a496bdd290b4c237feb6978f4ac`  
		Last Modified: Thu, 20 Jun 2024 18:54:27 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b394543393a2a139fd68790d0a3a2c56faefbe2275cbd2eeaa28acd2a7ffc1`  
		Last Modified: Thu, 20 Jun 2024 18:54:27 GMT  
		Size: 9.0 MB (8997112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e96ab6c97511c2aaaecad976debab598b5a41667cca5364bf771b03ef9b276d`  
		Last Modified: Thu, 20 Jun 2024 18:54:27 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:01f8ed54be9544131f32039b0dca8deb49eb614282019a03abe48fe4db851a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fed968a2abc94c1085171c6afc24f4d7df9c75621847b844bd084d17bd415c7`

```dockerfile
```

-	Layers:
	-	`sha256:80966fa8a44fbd428632ca1b2a54c8bf063d45ce49c44b2a3269a68f8fd40748`  
		Last Modified: Thu, 20 Jun 2024 18:54:27 GMT  
		Size: 176.6 KB (176573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eec929ba30aa9ca0b1365785fd53c3dfe1dbb3488d57ac461ae600aa53dcc05`  
		Last Modified: Thu, 20 Jun 2024 18:54:27 GMT  
		Size: 20.8 KB (20797 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:94505474d0bec622b32d659aa2a2eac4b88e00cd30e195e4ae77f763d753d7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15871672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b68d7666f6040092a26bfdd0c9e7f83ac364dbbfab4bee9847024cc09c8616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b114343c0924c3129115065cd6dafe9e061d0db81cfba62c981b9de353864dfe`  
		Last Modified: Tue, 11 Jun 2024 08:00:08 GMT  
		Size: 295.9 KB (295879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43760228defebd1601cd4911bcc7510a7dc1877f3cb1d059b3b4b6340a7db94f`  
		Last Modified: Tue, 11 Jun 2024 08:00:07 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb69a881bcec458806dd3a27f24ed56d80653545bcda02e173b0b8c3846e4b`  
		Last Modified: Fri, 14 Jun 2024 20:33:33 GMT  
		Size: 12.0 MB (12004494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a186cfd7d9293f5b78877e223edcd6d8d18e33b9d3557fc08afa9deb306bcdd2`  
		Last Modified: Fri, 14 Jun 2024 20:33:32 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:118f395e94e7372802de23bbf92e5bb467526048517adbf3a5059a0a4fb36846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 KB (195640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23097dbc317e9f7075a26ba6c36904748f384f43ec4e9f4fb60ebc32ec7651f5`

```dockerfile
```

-	Layers:
	-	`sha256:f428c2a5405d0880305fd0a0a9c01bff23be20702bb9ae2cbd845391748c1038`  
		Last Modified: Fri, 14 Jun 2024 20:33:32 GMT  
		Size: 174.7 KB (174721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bfc89cc06fb7b0cc331d20d8de8125cec29e385a6ad9e7eb55c79b7ffb2c7f`  
		Last Modified: Fri, 14 Jun 2024 20:33:32 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:1ad00d08e6e08cf11284097a7f00de8764bd50c3bdd1855bb493f4f6c51ae7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14644212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978271b08232ea601465d9039422d09d5a3a926898a3a1e37fe39b590a5dd09b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8faacf069a0bd9eaf8b7304f6a9a467efd9e7c339e09e8d0e5d4636f948e9c`  
		Last Modified: Wed, 12 Jun 2024 01:16:21 GMT  
		Size: 293.2 KB (293170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f5247fdcfbb1582fa898cbdf825717311f9da5c3de7af09923efa3948d5671`  
		Last Modified: Wed, 12 Jun 2024 01:16:21 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de46c80d51948d6d00379f25eed266cbe32e02b49ef037a8bf1c68e819f4105`  
		Last Modified: Sun, 16 Jun 2024 05:07:53 GMT  
		Size: 11.0 MB (10981019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13981b99130518932f1c2731f6639e97fc919f2288e671aede4c5511630f3cdf`  
		Last Modified: Sun, 16 Jun 2024 05:07:52 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:e7f4e31c3208c25a5952cc563d99ae51027f7de0527ea6b84485424c723da29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 KB (195636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e9c7d4432210f40485b027e01ad59f3071792a8f2bd2b466ff3597588a68f2`

```dockerfile
```

-	Layers:
	-	`sha256:92643aea24bbb261352772ee2d121f9fe2bef88580b443d9d241a7398ad49f5f`  
		Last Modified: Sun, 16 Jun 2024 05:07:52 GMT  
		Size: 174.7 KB (174717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03117fc80da42c1cfdc7409f7b97014c8941ef762d672ba74158ae070e1078c3`  
		Last Modified: Sun, 16 Jun 2024 05:07:51 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:fc9e6225fd810627f1c818b370e0997ed21df1faea04a73e8d176d984b009ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15361519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482c51bf0319752e7769bff676f670cdf798e5ef8011f3b20552fcae8315954c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_VERSION=3.0.2
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.2.tar.gz
# Fri, 14 Jun 2024 16:50:59 GMT
ENV HAPROXY_SHA256=9672ee43b109f19356c35d72687b222dcf82b879360c6e82677397376cf5dc36
# Fri, 14 Jun 2024 16:50:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 Jun 2024 16:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Jun 2024 16:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jun 2024 16:50:59 GMT
USER haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 14 Jun 2024 16:50:59 GMT
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
	-	`sha256:46bff7a63f7c2225752707dc2e41d014f8a11e9328547a0b9093e26aa081fd4f`  
		Last Modified: Fri, 14 Jun 2024 19:55:10 GMT  
		Size: 11.6 MB (11606316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12b305e0732fd51d610fde23ffaddc01843ec2d15fd3bc3281c2f24d6c5d743`  
		Last Modified: Fri, 14 Jun 2024 19:55:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:6ad2344414b05ec67489f34071b689333dc65fc68a4e9ef0bd69370326bc9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 KB (195516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9a40bb1b46357573ec361ace67d650e65f50593638bb54d8f2f2aef6b3d4c5`

```dockerfile
```

-	Layers:
	-	`sha256:068ac5ce66089ffb284adcbf3b9875305e6f3bac2017906ada961a6f2b296897`  
		Last Modified: Fri, 14 Jun 2024 19:55:10 GMT  
		Size: 174.7 KB (174663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb8549fa21aad7810394cdee1b544fd2aa899c55d798329e7c44204e4cc808d`  
		Last Modified: Fri, 14 Jun 2024 19:55:10 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json
