## `haproxy:alpine3.17`

```console
$ docker pull haproxy@sha256:59e0ebe842270109e928e034cdfc097e5bbf96be938cc70712af039b7f325b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:alpine3.17` - linux; amd64

```console
$ docker pull haproxy@sha256:0082e695c769ef42828628afd310c99c3f0beb554af1260665ecb710c629a057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11060406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a213d07f00d8ef6ef53d1a4e46b2958cd753afe3e7c67c1221f40035d7d64dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:31:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Sat, 11 Feb 2023 08:32:03 GMT
ENV HAPROXY_VERSION=2.7.2
# Sat, 11 Feb 2023 08:32:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.2.tar.gz
# Sat, 11 Feb 2023 08:32:03 GMT
ENV HAPROXY_SHA256=63bc6ec0302d0ebbe1fa769c19606640de834ac8cb07447b80799cb563dc0f3f
# Sat, 11 Feb 2023 08:32:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 11 Feb 2023 08:32:34 GMT
STOPSIGNAL SIGUSR1
# Sat, 11 Feb 2023 08:32:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Sat, 11 Feb 2023 08:32:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 08:32:34 GMT
USER haproxy
# Sat, 11 Feb 2023 08:32:34 GMT
WORKDIR /var/lib/haproxy
# Sat, 11 Feb 2023 08:32:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e913e2b2950ea69e88caf2f813e3f4dd937cea8e496616c2ff0cc6e3bbc1440`  
		Last Modified: Sat, 11 Feb 2023 08:36:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da64d0e411b6462a69dd089359386f2fb5abc6f41cdc7202057790f60764778a`  
		Last Modified: Sat, 11 Feb 2023 08:36:56 GMT  
		Size: 7.7 MB (7684232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a979219950b99f011e7e39c651ae59cf7f3997bb825d9dd6221db6761be6211`  
		Last Modified: Sat, 11 Feb 2023 08:36:55 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine3.17` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:6539c8f5cae4667d83cf3c648b52478f54fc64a1e468deab890b89d3f0fe2f93
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10633522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae9807fb0033fc139c593e3fb6d77ab275060396a46335f0b35d7716843efcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:07:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 14 Feb 2023 18:50:26 GMT
ENV HAPROXY_VERSION=2.7.3
# Tue, 14 Feb 2023 18:50:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.3.tar.gz
# Tue, 14 Feb 2023 18:50:27 GMT
ENV HAPROXY_SHA256=b17e51b96531843b4a99d2c3b6218281bc988bf624c9ff90e19f0cbcba25d067
# Tue, 14 Feb 2023 18:50:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 14 Feb 2023 18:50:57 GMT
STOPSIGNAL SIGUSR1
# Tue, 14 Feb 2023 18:50:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 14 Feb 2023 18:50:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Feb 2023 18:50:57 GMT
USER haproxy
# Tue, 14 Feb 2023 18:50:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 14 Feb 2023 18:50:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aacb0de7054b9a4e3119975b647a4677c10cdfb5eee0301d5b9ff639f894df3`  
		Last Modified: Sat, 11 Feb 2023 06:14:22 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f2bf629e715a492d571e6f269b7fd3831d84171cd4a3a876550bd30e96b128`  
		Last Modified: Tue, 14 Feb 2023 18:56:14 GMT  
		Size: 7.5 MB (7520935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847a2d688ca3e0e9d84f34e7d925aa57dd85c7e77c0a3e648cb6dd370b0b9a1`  
		Last Modified: Tue, 14 Feb 2023 18:56:13 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine3.17` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:d092d9d3e854ada44d3861be28198f482a51545e9c8dab023b630648a8969904
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761b540117bbe9f9cba5bc2450e1137df86326c175cd8b4f932d3ff16b25ca1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:39:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 14 Feb 2023 18:59:48 GMT
ENV HAPROXY_VERSION=2.7.3
# Tue, 14 Feb 2023 18:59:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.3.tar.gz
# Tue, 14 Feb 2023 18:59:48 GMT
ENV HAPROXY_SHA256=b17e51b96531843b4a99d2c3b6218281bc988bf624c9ff90e19f0cbcba25d067
# Tue, 14 Feb 2023 19:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 14 Feb 2023 19:00:14 GMT
STOPSIGNAL SIGUSR1
# Tue, 14 Feb 2023 19:00:14 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 14 Feb 2023 19:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Feb 2023 19:00:14 GMT
USER haproxy
# Tue, 14 Feb 2023 19:00:14 GMT
WORKDIR /var/lib/haproxy
# Tue, 14 Feb 2023 19:00:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185adf36e47e661c218e99a5dc2db7bafb8926606269feff5f2138448401a729`  
		Last Modified: Fri, 10 Feb 2023 22:49:47 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8efc7764056c06e272dc84b8e93a1d2e9e1c0bc3d4ce6ca3c94216e98e1e3a7`  
		Last Modified: Tue, 14 Feb 2023 19:10:09 GMT  
		Size: 7.4 MB (7424034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b4ffef54105e55ff279a66a3fd5658bbd8784e5c955fc8c37c247b08af5648`  
		Last Modified: Tue, 14 Feb 2023 19:10:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fb46bd5256040e0f9bbf89f4ff6380f51ea7fe06cf4e1dddd740778c059abe8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10844647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4952fab450945a5f63bd867c51c0f89973cf52ef078c4ba48c51db62b442306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:46:12 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 14 Feb 2023 18:41:04 GMT
ENV HAPROXY_VERSION=2.7.3
# Tue, 14 Feb 2023 18:41:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.3.tar.gz
# Tue, 14 Feb 2023 18:41:04 GMT
ENV HAPROXY_SHA256=b17e51b96531843b4a99d2c3b6218281bc988bf624c9ff90e19f0cbcba25d067
# Tue, 14 Feb 2023 18:41:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 14 Feb 2023 18:41:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 14 Feb 2023 18:41:25 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 14 Feb 2023 18:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Feb 2023 18:41:25 GMT
USER haproxy
# Tue, 14 Feb 2023 18:41:25 GMT
WORKDIR /var/lib/haproxy
# Tue, 14 Feb 2023 18:41:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3ef51ac36ef103e2d0b304a2a22a5f29683e7a5873d334fc29089b9c750f79`  
		Last Modified: Fri, 10 Feb 2023 22:50:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d19cf7183918ef820e2d01ef869e395d8a90ab9beb3ca6223041527087f1e7`  
		Last Modified: Tue, 14 Feb 2023 18:47:47 GMT  
		Size: 7.6 MB (7580957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147138744b055c75e704b778c8e63afd8bfc797aedf772fef07fe4f65091fca8`  
		Last Modified: Tue, 14 Feb 2023 18:47:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine3.17` - linux; 386

```console
$ docker pull haproxy@sha256:45e14ffc096c982bd5e0773ee19d3e4fb0b5b18064e8e3042fde4a861e84a24c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10893732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd22b8042ca6618c799c7063bbd70f96e7487f74cd369e789431c43ffe27ce3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:23 GMT
ADD file:125f3514520a5cd29df2830a409aa026a2bc06a77a7a5d150133436404b33d41 in / 
# Fri, 10 Feb 2023 21:24:24 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:35:21 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 14 Feb 2023 18:43:19 GMT
ENV HAPROXY_VERSION=2.7.3
# Tue, 14 Feb 2023 18:43:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.3.tar.gz
# Tue, 14 Feb 2023 18:43:21 GMT
ENV HAPROXY_SHA256=b17e51b96531843b4a99d2c3b6218281bc988bf624c9ff90e19f0cbcba25d067
# Tue, 14 Feb 2023 18:43:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 14 Feb 2023 18:43:53 GMT
STOPSIGNAL SIGUSR1
# Tue, 14 Feb 2023 18:43:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 14 Feb 2023 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Feb 2023 18:43:56 GMT
USER haproxy
# Tue, 14 Feb 2023 18:43:57 GMT
WORKDIR /var/lib/haproxy
# Tue, 14 Feb 2023 18:43:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b3e346c15c2377ec0e75cc9efa98baecd58b0e9bb92f0ec07eeda0bcc7e67fc7`  
		Last Modified: Fri, 10 Feb 2023 21:25:13 GMT  
		Size: 3.4 MB (3412353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c5fa59dd895358f8af2563c1fdab7b4b953efc4b162b347ba89f0bac71c17`  
		Last Modified: Sat, 11 Feb 2023 03:43:05 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f190566afecea2633072c4213c123328238d3ef4caacdaf823ddd64d4cccb35`  
		Last Modified: Tue, 14 Feb 2023 18:55:25 GMT  
		Size: 7.5 MB (7479679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a2fcc6e81263bec6fa474900740621bfea3211eeef1ce328a0ad9da21abf1f`  
		Last Modified: Tue, 14 Feb 2023 18:55:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine3.17` - linux; ppc64le

```console
$ docker pull haproxy@sha256:50be382470fdbf145d5beaa940d65ff4b97b1e558fdd338c5e8ba31cd1bc0558
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11441921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbfbfc780a7f9e8d3b1baedfad9f2469e8f75e79ccaa456449b2c2a00a2561b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:56:57 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Fri, 10 Feb 2023 22:57:57 GMT
ENV HAPROXY_VERSION=2.7.2
# Fri, 10 Feb 2023 22:57:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.2.tar.gz
# Fri, 10 Feb 2023 22:58:00 GMT
ENV HAPROXY_SHA256=63bc6ec0302d0ebbe1fa769c19606640de834ac8cb07447b80799cb563dc0f3f
# Fri, 10 Feb 2023 22:58:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 10 Feb 2023 22:58:35 GMT
STOPSIGNAL SIGUSR1
# Fri, 10 Feb 2023 22:58:36 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:58:38 GMT
USER haproxy
# Fri, 10 Feb 2023 22:58:39 GMT
WORKDIR /var/lib/haproxy
# Fri, 10 Feb 2023 22:58:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf2eef4c44e665d033d670a4b0c6251ca72cce8570611f665d290043aa23c2`  
		Last Modified: Fri, 10 Feb 2023 23:04:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001786f9904b8af3ac2cfd6552e1ae58e71a42aab9ba22582eaf18000544067c`  
		Last Modified: Fri, 10 Feb 2023 23:05:22 GMT  
		Size: 8.0 MB (8049439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a57be633ee629aff58b7989a611395d27510e6af9ad533762bbab4041a01b8`  
		Last Modified: Fri, 10 Feb 2023 23:05:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine3.17` - linux; s390x

```console
$ docker pull haproxy@sha256:bd924d56cf8177820c36d9ee7bd19873a5aeb2757415946895ccac359e0a213d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10675786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a6f33fd96976f1f7338e5b14c0d4a1ce172873910ee48b44004e180938e37f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:23:38 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 14 Feb 2023 18:44:14 GMT
ENV HAPROXY_VERSION=2.7.3
# Tue, 14 Feb 2023 18:44:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.7/src/haproxy-2.7.3.tar.gz
# Tue, 14 Feb 2023 18:44:14 GMT
ENV HAPROXY_SHA256=b17e51b96531843b4a99d2c3b6218281bc988bf624c9ff90e19f0cbcba25d067
# Tue, 14 Feb 2023 18:44:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 14 Feb 2023 18:44:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 14 Feb 2023 18:44:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 14 Feb 2023 18:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Feb 2023 18:44:45 GMT
USER haproxy
# Tue, 14 Feb 2023 18:44:45 GMT
WORKDIR /var/lib/haproxy
# Tue, 14 Feb 2023 18:44:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8690c2e368feb551d931f60e4d5d0513a2a251ba61ecb5ab9f9c485a6c8cbb`  
		Last Modified: Sat, 11 Feb 2023 05:31:58 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b8e45b9cbbd857f22cd03c14fc591b85a03de62d97ca70744dd8b75312c923`  
		Last Modified: Tue, 14 Feb 2023 18:53:07 GMT  
		Size: 7.5 MB (7498942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afc1d88144b4857ae65bcd67a35bb12728d1cc7a59720940b2b5b4f75af8375`  
		Last Modified: Tue, 14 Feb 2023 18:53:06 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
