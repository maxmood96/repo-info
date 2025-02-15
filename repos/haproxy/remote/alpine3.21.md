## `haproxy:alpine3.21`

```console
$ docker pull haproxy@sha256:54a9bda49fb275fb648afc5e4f81ed86218337434c22946c15247a681af033a8
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

### `haproxy:alpine3.21` - linux; amd64

```console
$ docker pull haproxy@sha256:545c9b92520454a1d975301e039862b76d0e230834012e89fd332a2e993bd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0348043c80aa31809ee5991984187e15f27a75c991e477fee2064dd7de2d6bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a72af70cd183b96888a5ee1cae5a5d7cb2de32ce857f5411f9f211c7bddcf80`  
		Last Modified: Fri, 14 Feb 2025 22:59:23 GMT  
		Size: 294.9 KB (294879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aa0b723f7384b242ec035a5a10b38cf07f6d6d78709a8f706f4b043ba33f9`  
		Last Modified: Fri, 14 Feb 2025 22:59:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c361d29bc18ed2d66ea350471f7f9dcd08d071f9654c07b06cd4823af36b477c`  
		Last Modified: Fri, 14 Feb 2025 22:59:25 GMT  
		Size: 10.1 MB (10142141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1060491eb601518ff8a9c2ab66da0bd7d2e0ed5ac9fa56ef0e1d2abbeb8db0a5`  
		Last Modified: Fri, 14 Feb 2025 22:59:24 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:aed84c0689fd96011669d29b3fe816512af093592b17b903c34f02d6376b0f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 KB (206789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8843645e0918a56b52451720bba53d90e0e0d142f4c42f17faf27ec16b438b9`

```dockerfile
```

-	Layers:
	-	`sha256:d11b9dcb9dafdc9574713d1740720a51a1da76a5c19b42823c1761595df10e90`  
		Last Modified: Fri, 14 Feb 2025 22:58:27 GMT  
		Size: 186.3 KB (186339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bb7eaf0f4772f642621e1e3154874184ed71d186d213afb93f766fc2783047`  
		Last Modified: Fri, 14 Feb 2025 22:58:28 GMT  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:f5a8d0a1bac9015b084e909e7d9e779613e449838e908d2ee9933dd02c641c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13829472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71dbb02edb17e305cfd33b915f40691d87dcce96b733e8d2d2ff18802bec68c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687a14ad260fb4fc6db1f0c86d25e09804f3d50a74985686018c2f56f7dd8e7`  
		Last Modified: Fri, 14 Feb 2025 22:56:04 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16df665dca9b0f015404e24fbb55fbf1e84f5db281481cb4a0039b142b0104f1`  
		Last Modified: Fri, 14 Feb 2025 22:56:04 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19936c1848eecec6cd19f8ac66adabd34795e4a05e5bf7ec13e622c11e673ae3`  
		Last Modified: Fri, 14 Feb 2025 22:58:45 GMT  
		Size: 10.2 MB (10167059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6deab4553873a8a3abc9cfb950a9da376804d6a08c303f37f3c0dc9a655b5400`  
		Last Modified: Fri, 14 Feb 2025 22:58:44 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:05d0b1cad5430ec5aa606c8e47c8fb620c2adc88969d03ad415b1a9497caa511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca033713244fdfda2575292085bb5efa74a55bccfdb5c3c1c184661d004ecf`

```dockerfile
```

-	Layers:
	-	`sha256:8b3cb3fbd5d12c8a5ecdca11455cca5765d4bd6a52862870741e057a787c179e`  
		Last Modified: Fri, 14 Feb 2025 22:58:29 GMT  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:d804c3ad15b4ff97dd0547a9513a4be69808a67d9c99b658edfb79a84b119202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13406830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0200c35d53c1670039c9ca6acef6cfa50be89b8b80a0eca7f4c2b2b1ec82b742`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510a4ca166402494f4446a67668b9451a59e7fc3a52d6f75a82f0f5e8765808f`  
		Last Modified: Fri, 14 Feb 2025 23:32:18 GMT  
		Size: 295.2 KB (295186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997b631db78d26a36cacdaec7a75f0bc011ca691253882b64e0cae631d3e84d7`  
		Last Modified: Fri, 14 Feb 2025 23:32:18 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db9598fbadde497b24fb9aa3d0109f640483960e8a7ed5a34468fa98fb28b4`  
		Last Modified: Fri, 14 Feb 2025 23:32:00 GMT  
		Size: 10.0 MB (10012086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bfb81f33c220b916824165b4f3634027613147723d669f80d617d37f12dba4`  
		Last Modified: Fri, 14 Feb 2025 23:32:18 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:4136acd9c5d83a2697d6f39bc81a1bea3754b38c81dafb6a96a4ef269c0397cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 KB (206959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f70e3034a90f4117e24b38aaa588320f3ae0e4c8af4b30093948a843fd38d1`

```dockerfile
```

-	Layers:
	-	`sha256:194086b3df3e3b75b7bedc5733313be08f7a2dcc7779902d8a2ff30264b72721`  
		Last Modified: Fri, 14 Feb 2025 22:58:30 GMT  
		Size: 186.4 KB (186391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd22161699f010df7b0400f8e6bb1bc55ce99b46536c15a9336c1c80ceb5159a`  
		Last Modified: Fri, 14 Feb 2025 22:58:30 GMT  
		Size: 20.6 KB (20568 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:08f50e7324a88007d2f9445d1cd4bff8c4485482c6e0ed858fa4eb2fd9e932cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14361806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3b36598774c145a110a2c70966961a500130292e898e3be07c5edafb6bba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ff377e941b8dc07fa2758cd64ecb3180fd4f1f46eb102646984c24baee564`  
		Last Modified: Fri, 14 Feb 2025 22:46:40 GMT  
		Size: 297.9 KB (297854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57938811f0ed4bd1a515443a08ae58cd2b0038cc24927e2fc4e9a3db261a20c7`  
		Last Modified: Fri, 14 Feb 2025 22:46:41 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4da969a08bed8654a9c97abda16903f7647c8ef7ba556f76ed1e642ca63bd0`  
		Last Modified: Fri, 14 Feb 2025 23:00:06 GMT  
		Size: 10.1 MB (10069482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43fe7af79813b9ceeceea7e85b7a7edf91f3c828399989c202c7aac2a5647cd`  
		Last Modified: Fri, 14 Feb 2025 23:00:06 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:c8776b0d34e4265ff60ad6d9657eb776fcea1ed68049b34ab35d066cf586fb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 KB (207027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaca1905351374554227e3e35f82a96a440650136ff8d6c68e5ba2506b9078aa`

```dockerfile
```

-	Layers:
	-	`sha256:3ad7718210ee91e6fac693d13b0b6fdfb4f7ca3fb21b50dac0d8b6990f5f5e18`  
		Last Modified: Fri, 14 Feb 2025 22:58:32 GMT  
		Size: 186.4 KB (186419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fce69454083c55d1d9ab4a8df841ffe633a7e01e13ec9d58f96687f5b25ef88`  
		Last Modified: Fri, 14 Feb 2025 22:58:32 GMT  
		Size: 20.6 KB (20608 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; 386

```console
$ docker pull haproxy@sha256:dfedeb114b3776791ee45962495ceb9593bc88b1eb8763f762b1fc921ee28059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13654511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa1a1fceb3312771480f2d31f8ac21f2f276f8bf03287880a30556591f2e1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b90e1b7bacb80740af6ee31dfea136a5a302c3645e825afaaf1cb1e48cb587`  
		Last Modified: Fri, 14 Feb 2025 23:32:17 GMT  
		Size: 295.6 KB (295584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da79fe45b070c374a77efb965840d4e5c2c4111ac0b2427e07ce5d33c437e37`  
		Last Modified: Fri, 14 Feb 2025 23:32:19 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831ade9dddb88408ee2feff3b971644216cb0d26e6289431436e313715aed8ee`  
		Last Modified: Fri, 14 Feb 2025 23:32:02 GMT  
		Size: 9.9 MB (9893869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5840e9d972a0b5f67fd398d1f730ccf0882ae9e8b23edaa59eae395e1adc505`  
		Last Modified: Fri, 14 Feb 2025 23:32:19 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:7224133344c0f4ac0c24c51d4ea02dea8172761302a0d9dde99ab0f15654c4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 KB (206705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5bd2d338c5cf803221c725889009dca64360b6ccff78bb7c90e5d1c721d1bf`

```dockerfile
```

-	Layers:
	-	`sha256:161faa174652a2536cfad95114f3e8fbf00a09b9aa22491a9ea382938be9c23c`  
		Last Modified: Fri, 14 Feb 2025 22:58:34 GMT  
		Size: 186.3 KB (186304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e972096d94e7dbfb1dec8431cf066a72f4ff14de7e2ae1e17dd88086f6b96db`  
		Last Modified: Fri, 14 Feb 2025 22:58:34 GMT  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; ppc64le

```console
$ docker pull haproxy@sha256:13731feda008d76629ea093a2f2a997ca1724490ed79c3cbfa6abf476bc9d26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14517924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f277396bd4d6652961a84816386b51ab2145850271ae5507dcfd5f66e88c9c37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e804408de2cf4c723cab8b38ea4afbcdb2cfa4d1ad3d84d2ad4cf2848b74ac`  
		Last Modified: Fri, 14 Feb 2025 23:32:13 GMT  
		Size: 298.3 KB (298269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928e2b85fff2cbd0114b27569e94a7dbc3dab7a844aadad77a7d5b7efd809199`  
		Last Modified: Fri, 14 Feb 2025 23:32:13 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986985b0345a5727343c28c2f415023e0b119d512d4c901ed2a28fc39b01358c`  
		Last Modified: Fri, 14 Feb 2025 23:31:54 GMT  
		Size: 10.6 MB (10643870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1fe64a87cc4bb52139f41097b3d1c5e70a2d5bcdf7ece4b582c83a59a6e3fa`  
		Last Modified: Fri, 14 Feb 2025 23:32:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:b30de436d8526abf63d1da15adf0e0e62fd1f37812de41a37712f2fc6b01ccd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 KB (204944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2298b101a05001d275367180acee6be88ce81ef9181b60ee8dbdf209b99dbd92`

```dockerfile
```

-	Layers:
	-	`sha256:7c59160c05909f286f528a8c499d8c9086e768dc77df1d99395e9e8285950263`  
		Last Modified: Fri, 14 Feb 2025 22:58:35 GMT  
		Size: 184.4 KB (184434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ec3c57766089653442f5b55f482bde65ab6fa7d910f236ad1ad6a8b2b76acd`  
		Last Modified: Fri, 14 Feb 2025 22:58:35 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; riscv64

```console
$ docker pull haproxy@sha256:ede3f5d02cad57bcda2283ede7dc6bf6bc0fcf4947b2992c56f04ee43932154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13409852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fe20221fed6055bb9649277611df17627bb04b09090447e6cca0bc0fe35db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22171ce9b4c4f3b6879cfc2f72d965a79cdb9074a5b06c77c217e1981dae2e2d`  
		Last Modified: Fri, 14 Feb 2025 23:32:09 GMT  
		Size: 295.4 KB (295351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65efa07118c7ad2eae25639ed9a9d25b87ce01b795b0b74cc8fda0267ef465f4`  
		Last Modified: Fri, 14 Feb 2025 23:32:09 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef11144f43ba568ecb3da2e4c7ddb99bd81235d707d1f39d91da8e2e9d361fd`  
		Last Modified: Fri, 14 Feb 2025 23:32:04 GMT  
		Size: 9.8 MB (9761621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de2832bb96d3c8dbd679efbd6e21bfb17d37da10628f23ad33e7686c37e1a2`  
		Last Modified: Fri, 14 Feb 2025 23:32:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:d9f3f3133b17cf1d5a700e3ea3b0126be8e7a5b8cf9a67b112f091e3a3dd9c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 KB (204937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde61647b43acd258e0472c3ed0f73f916218db7e38cfaf04c39678e3e4d70a2`

```dockerfile
```

-	Layers:
	-	`sha256:05073555ad110dbca0af3b7edab47a876f01b80171459b44442eab351690cae1`  
		Last Modified: Fri, 14 Feb 2025 22:58:36 GMT  
		Size: 184.4 KB (184430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab9ef8e455be6a57c257cf84fd0f5c790f19c52985ac1bc5f49c29887d80834`  
		Last Modified: Fri, 14 Feb 2025 22:58:36 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; s390x

```console
$ docker pull haproxy@sha256:2e235e9920e404fd410321e97ae60abe96e585f46001202dfa37ca2952f0a18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174ebb4601ac50cca64579d0301cda8f3a3063f2a818a1559fba851dd64c15f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 29 Jan 2025 18:24:27 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1d6fbbaeb31150829b61c97bf95a54dd80af8879ff0c3eb389deae2e014d40`  
		Last Modified: Fri, 14 Feb 2025 23:32:14 GMT  
		Size: 296.2 KB (296184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b92d46335503c8ba202927115f72a2afa9a81d8a4bd523637b655ac0e2e26e`  
		Last Modified: Fri, 14 Feb 2025 23:32:14 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9e441845e05dbc1a671096a2fe736c0ca01645ac968da009dd04cd382cec3`  
		Last Modified: Fri, 14 Feb 2025 23:31:56 GMT  
		Size: 10.4 MB (10381644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7189750b6b5bd2d613ec98999c568ced7a544dcc58fa7fec05a2481bb3726`  
		Last Modified: Fri, 14 Feb 2025 23:32:15 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:8fb1109e1e5303c6dc5b0e341f81fe0ebd00c7954a66d08f863f1de2ae2ec7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 KB (204838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31be4486adb10f8f7c833a4287942fe830e727f1466fadc0cc3c5443796afda2`

```dockerfile
```

-	Layers:
	-	`sha256:65df00f67f891548aec0e09089f79e0fc717debcab42fd856486f6554b88de3f`  
		Last Modified: Fri, 14 Feb 2025 22:58:38 GMT  
		Size: 184.4 KB (184388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dff20f88c8e51c7e6376f8c47900f5486ec8a727601b28fe8a0d17cdb678a71`  
		Last Modified: Fri, 14 Feb 2025 22:58:38 GMT  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json
