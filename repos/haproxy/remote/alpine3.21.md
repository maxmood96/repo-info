## `haproxy:alpine3.21`

```console
$ docker pull haproxy@sha256:1023b900b1e141ff74a1a8450e1a86a74afb2c6853e4e451e014d826512daca0
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
$ docker pull haproxy@sha256:0c7cffc72397cbd1e4271bb17d58314a3132e6f936bb997774dc4f4244732b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14123785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e73aeaaac4205d09ba9a540a9f0710673146ccb9a3a6524d5c98edc1ff7790a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533557f3b9cf2e9a070a95c8837f9fde879a00c266f1867325e98e9a5dabe71e`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 294.9 KB (294905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4509f5cb2f806e56127c7c96f3d116805a161db8d8ecb6b469ad8615d1b4bea5`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10da6247fb51e2c2853dfb52e930bde9852737b4cfbf07be4b70c73133ce7416`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 10.2 MB (10185195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d54acade7888e0dbded43347b27fff2bba4ca68529d739cbadcabbba3aeac70`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:2a61e125a0d33d1d836867fc6f6a373ad246d1f1366b1340d0de627706da4655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 KB (206788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e336ef8b79f6feac193cbbfdeab83c182a9b329a057fafaa5682d8609e109968`

```dockerfile
```

-	Layers:
	-	`sha256:3044265df3471a94d7d35add78d7b2fd6a0485dead0cf2c583a67d05618a1133`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 186.3 KB (186339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167e862fb9e086599a6a3eb491fa51035ae3fa33fc2130482ca9c0a7413af6eb`  
		Last Modified: Thu, 17 Apr 2025 18:30:39 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:29d79e637d3a383d923d115561f4a48f1b5f3cfda280f47acd98b487db797b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13938611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23f9afa63a7248c487d7b0ab046c61dc9ed0fbc45f6c7b252876e354c12fa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687a14ad260fb4fc6db1f0c86d25e09804f3d50a74985686018c2f56f7dd8e7`  
		Last Modified: Fri, 14 Feb 2025 19:48:24 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16df665dca9b0f015404e24fbb55fbf1e84f5db281481cb4a0039b142b0104f1`  
		Last Modified: Fri, 14 Feb 2025 19:48:24 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cd2a14d16a9bbaa60331ac7e5b218fbc0f94a5016a19191bd54615cfad8811`  
		Last Modified: Thu, 17 Apr 2025 18:38:29 GMT  
		Size: 10.3 MB (10276200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eed97df608af026824dc1e5c8ba1d26c53f4684652a6f40e7db74b6f0de4471`  
		Last Modified: Thu, 17 Apr 2025 18:38:28 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:273155b88e0d091b42d44eedd00852f7f23b92d0274969bfcb728340f608b84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8f3de8e77dedfa3afa39711e8705fc52561c1a9560265b5ac1141ee4cb5b6a`

```dockerfile
```

-	Layers:
	-	`sha256:c3fd9d30cfe6fb97bc80cd30317a6ff07b54574e8d7c5c3aebbad6025a27974d`  
		Last Modified: Thu, 17 Apr 2025 18:38:28 GMT  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5045c4402b466c8655f3c5245fb88af7926633bb4af03e1a72e8ccfae10e78c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13503367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d6a81c9b642001a99690a8a5566b3a4f4b1432b50fb030222def69246598a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510a4ca166402494f4446a67668b9451a59e7fc3a52d6f75a82f0f5e8765808f`  
		Last Modified: Fri, 14 Feb 2025 19:31:33 GMT  
		Size: 295.2 KB (295186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997b631db78d26a36cacdaec7a75f0bc011ca691253882b64e0cae631d3e84d7`  
		Last Modified: Fri, 14 Feb 2025 19:31:33 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63583ac821c640349a303c6fcf9fe975f3449a521268c966c3cd46a1cebbe3`  
		Last Modified: Thu, 17 Apr 2025 18:49:32 GMT  
		Size: 10.1 MB (10108624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b0ef6d38241c8d2f875bb642222937984c486645f22a7bc4e02fbf89a234a`  
		Last Modified: Thu, 17 Apr 2025 18:49:32 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:8b0bcdcbf29e0e03de3ee1bb43a94633c3bd1ca8cbc36427b53d9d82632a6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 KB (206959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98fd497db7c713a708f61dcc23ce87b84bd6b379cdc23bc5b00472c4f1aae32`

```dockerfile
```

-	Layers:
	-	`sha256:6969ab231bcaeeb93cb008aa1c1eb0002e410f7ab787aed0f32de69ce8f110bd`  
		Last Modified: Thu, 17 Apr 2025 18:49:32 GMT  
		Size: 186.4 KB (186391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e7165a81a76334e8d9097a5c2c9a431fa2146cecca4303712ea1ac95639a5a`  
		Last Modified: Thu, 17 Apr 2025 18:49:32 GMT  
		Size: 20.6 KB (20568 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f4fa5989ca68da0c63c1331e6ac68ebf1bac668d00ca1090e71ecec79de04367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14400493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c4a3a1aec8c9f9352cf3809307381a76b07ea3f3295700515af378d2aaa0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea497ce686fe9263ffb10559a67b8d89baef486df5a707a561f5bd0400bb8f7`  
		Last Modified: Thu, 20 Mar 2025 17:53:55 GMT  
		Size: 297.9 KB (297866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2202d6196566a0d7016bb3fac2259cf9c8e67cce03c3ff641b4573ecb337fd91`  
		Last Modified: Thu, 20 Mar 2025 17:53:54 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca529191ad4acc0eac5f241c72533dc69c5fd0549211aa8ce13643b66cd23677`  
		Last Modified: Thu, 20 Mar 2025 17:53:55 GMT  
		Size: 10.1 MB (10108157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21fb215077ae2cf9162524cc7370f8a557a50ca4725b49115d0433bd335cb6`  
		Last Modified: Thu, 20 Mar 2025 17:53:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:74b35a876bfeac065a718cbd3249b17f5d7deeaa5e1b50b4a94a8ab0573d85aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 KB (207027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7860e89fa43fcc8a1129663c7a1a0718afee2a4408fcb30861373a04b37130d`

```dockerfile
```

-	Layers:
	-	`sha256:42e492fb5930907ba8c70f358108ee75b803e19795df4854424ef38cb84a8eb4`  
		Last Modified: Thu, 20 Mar 2025 17:53:55 GMT  
		Size: 186.4 KB (186419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf7d454c5c7638a3d50a4fa74e836bd17394fb25f4070e487140a12b8eb653f`  
		Last Modified: Thu, 20 Mar 2025 17:53:55 GMT  
		Size: 20.6 KB (20608 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; 386

```console
$ docker pull haproxy@sha256:be6309b8cc7cb992143a2c8c08affcccb723f1c37743c74b1787ec740d9cd279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13696096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47fa735ee9331c2ae7c1305e48ce02450aef6e4a019987e2a7344737c4fa935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066f11a6a240414e8998b0fc16e791a3d61230f216f81ed8e74a581c2e638980`  
		Last Modified: Thu, 17 Apr 2025 18:30:59 GMT  
		Size: 295.6 KB (295604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb1e68d4eee42d90a8ffa9c0dbebb7fd4bd4b855a039a9e5380b11ca7809669`  
		Last Modified: Thu, 17 Apr 2025 18:30:59 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf115a05d439ccbe1988615cf6174491bdc63d2157987cbcd75c3da33ea59e6b`  
		Last Modified: Thu, 17 Apr 2025 18:30:59 GMT  
		Size: 9.9 MB (9935432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56007d2f64cfa81808666e489c4dbcec42159657ee38787d0f1794e4a8fac80d`  
		Last Modified: Thu, 17 Apr 2025 18:30:59 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:9902d4a37414d60d494a0e68183b2466f391105fbeb7bed5e4e1c9e9e9d52a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 KB (206705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32615c6da7bdbf4a59f9f2ab44f542b453edfbd646966640e458ce63e95ef9bf`

```dockerfile
```

-	Layers:
	-	`sha256:3653594f7d5069f59da1cfc42eb4063910407fc95469528c3290a40199cd4b7e`  
		Last Modified: Thu, 17 Apr 2025 18:30:59 GMT  
		Size: 186.3 KB (186304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35cd891ac64dd965046848a7f5b2219620489849a8c209086a53992fbe70e22f`  
		Last Modified: Thu, 17 Apr 2025 18:30:59 GMT  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; ppc64le

```console
$ docker pull haproxy@sha256:df2fe3582514c2ddd5cf4814fd6d09437011f9d00ece5aeaf7d7250a0d589a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14551073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758adea40d395461d08ca34a4b8cc1ab844df4ac9159530c3c1d76638135b933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6547228289d331d1273c2a943dda58236b5600503317a843cb9a02ab19da8356`  
		Last Modified: Thu, 20 Mar 2025 17:54:12 GMT  
		Size: 298.3 KB (298278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fae19d1e708dc54beac4bded631ac48e2c9da21ca43438bc6e72d3d249cf679`  
		Last Modified: Thu, 20 Mar 2025 17:54:11 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd0715dd864017ba59a38b942c7836a91c733e7db3e819696883f233a7e6ad7`  
		Last Modified: Thu, 20 Mar 2025 17:54:12 GMT  
		Size: 10.7 MB (10677008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f634163c469c78e1887852579111553d768298e954044a94e48df129e6b0389`  
		Last Modified: Thu, 20 Mar 2025 17:54:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:665200dfbc290780202a6de1a2494c353c54f62e5dbc6825815b411ed6b026d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 KB (204944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c631c5114235997ec99fa1d3b61ce2672deec44c98e51c7e114932e4f1a489`

```dockerfile
```

-	Layers:
	-	`sha256:00764c7e6edca6965c06c8d98103b911d439002a7f319e2cbf583373324a0be3`  
		Last Modified: Thu, 20 Mar 2025 17:54:11 GMT  
		Size: 184.4 KB (184434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e52b5cc3ae16fc0e06c60d631f4e66ad8ed659966497b00119c79df26360d47`  
		Last Modified: Thu, 20 Mar 2025 17:54:11 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; riscv64

```console
$ docker pull haproxy@sha256:b11833c8770cb9de1cc01f2e7db3757615d73ae58f3f4949a9f21f89f5487202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13439204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228f06778ebcfa894deb0d862052087bef2e6f00b7bb0421f0d87d4f796e0719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22171ce9b4c4f3b6879cfc2f72d965a79cdb9074a5b06c77c217e1981dae2e2d`  
		Last Modified: Fri, 14 Feb 2025 20:54:59 GMT  
		Size: 295.4 KB (295351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65efa07118c7ad2eae25639ed9a9d25b87ce01b795b0b74cc8fda0267ef465f4`  
		Last Modified: Fri, 14 Feb 2025 20:54:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d804ff4976ce1c93b2525e5245976ca04b67fad941c37e6fc50dc6e6772025`  
		Last Modified: Thu, 20 Mar 2025 18:05:35 GMT  
		Size: 9.8 MB (9790974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ce61c3c31bef941f1c6f49ed57aa31b6a261e9768b6c3843c2d014f00de24a`  
		Last Modified: Thu, 20 Mar 2025 18:05:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:6931d918fb4f87804c321d5cbaac60e3af389ab9ed8e69024a3ee8df4e412a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 KB (204937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e11d5f878314cced4e55e95e59c358cc7509b92488affad150b52064b616b5`

```dockerfile
```

-	Layers:
	-	`sha256:7672320608d627d7f83b52424b356b37f06c68f1fd4b5b0b670243995819ed88`  
		Last Modified: Thu, 20 Mar 2025 18:05:34 GMT  
		Size: 184.4 KB (184430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e565790e9c0844f36c1bdddc9ab0a46b9feb745754741696ebf0c21ec984f252`  
		Last Modified: Thu, 20 Mar 2025 18:05:34 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; s390x

```console
$ docker pull haproxy@sha256:e1b7938fd97b07eb5628876aae0dab837ca2d46835a616f8155d8fa625318029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14179129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f494dd2727ab9b6ffc939014cc0dba375c5167c9f43276a3fe569b0d3e20656b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799900d9d9f0fae00a426b9c0da20ac257f0ff703151ac4ee425e2a98945d8d7`  
		Last Modified: Thu, 20 Mar 2025 17:55:50 GMT  
		Size: 296.2 KB (296190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772438863f57ef3e2e7f726cddcb180d9295aac8d42cc03fdf63dcdd1cda28d4`  
		Last Modified: Thu, 20 Mar 2025 17:55:50 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab4c2037abb3e32bbf08561a602143632134ca48f682f9e5ea2c229767785b`  
		Last Modified: Thu, 20 Mar 2025 17:55:51 GMT  
		Size: 10.4 MB (10413929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4607441638081944a619455746b47311518d370f3439bd93768d739c81cb383`  
		Last Modified: Thu, 20 Mar 2025 17:55:50 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:c1360b90a0b49d50a6b371ec1e129d3d21afed63095ae058528a76bcc5e1fe9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 KB (204838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ff45709112c952bc083d64b60cf23c03dbe6045f109ee10b13033a9fc482eb`

```dockerfile
```

-	Layers:
	-	`sha256:28bc00a2d1b4658ba744662f49e2106b4c8b71bba79978ddbe1c67dbe25c0da1`  
		Last Modified: Thu, 20 Mar 2025 17:55:50 GMT  
		Size: 184.4 KB (184388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fb9d4c33c9f00948fc420d44eec52360fb47ec17f20eac7829ca0a93452075`  
		Last Modified: Thu, 20 Mar 2025 17:55:50 GMT  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json
