## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:844de6668d34289997196221377744284be21f7c605d164555a64075af78aa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:e52a23671e6001a13fb6cda7e24c5c38b067c0bfd3c8ed0f60135ad5275d83b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c5e18809d3a465e3467a58acb6f7b8c51b82107ac3ca8251ec5cc77bb1b137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dfbbbef8da69c1869eee5657b3695d1f33af787dea04e1b718ca441b1ebeb8`  
		Last Modified: Wed, 20 Mar 2024 22:01:23 GMT  
		Size: 990.4 KB (990357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844836e9dccbed49f73106913bcd65508e74a6e54e334965c724e43ad5bba24`  
		Last Modified: Wed, 20 Mar 2024 22:01:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217fa87131785efaf9e094bd4d494e7026b4a19a6dec28c3c3262bbad27b914`  
		Last Modified: Wed, 20 Mar 2024 22:01:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:313cd8e14bedb3b6a0a5e1d34db88c1fc79fc8673c215ea27e89252fb8779959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12fcf5876c242f966502d6163556c7a2eb77e22136e68d51a3e6f48fe1c0045`

```dockerfile
```

-	Layers:
	-	`sha256:1e5aab9ca4d9669d1a10af252287e07a62656b665aff933952b17f65a878df6c`  
		Last Modified: Wed, 20 Mar 2024 22:01:22 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef803d4b42ddaa9622d8b71d4bece9fc693763dcb5eb44bd0b9cac923b61fbb`  
		Last Modified: Wed, 20 Mar 2024 22:01:22 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:e7278040cd88a1be6e6d9e7b6e90f9bef2c1c26551d2ff10b7de92448d2abb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06494f8f692d1c030f1fc5cf838975c967e7f64fba05055db4b540450dc0803`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc86cc87d5563a8acd2790ba080c0b6e5edcb47e159da8273f9023d1134d607`  
		Last Modified: Wed, 20 Mar 2024 23:10:44 GMT  
		Size: 975.4 KB (975395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa4bf3885d3becdbdeb4eb0a501c4b926e5ab546017f9b042674c22435aeda2`  
		Last Modified: Wed, 20 Mar 2024 23:10:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309f29826691b851c70aef16bbd5aa5a6bb62a95b1babd66d93481ee1407f8c0`  
		Last Modified: Wed, 20 Mar 2024 23:10:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:dc50103fd63d00a43c7d361a564b802f4cbccc71420dd5adea2c77b93049238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217acd967bec0f69167e2b6ec3fe4bb02175af8ae6b66ded052b62c199040d10`

```dockerfile
```

-	Layers:
	-	`sha256:be69fd43ca06ad751d441abbf50fa7e2b0c7e5fd3fccb40f71bb4afa83153544`  
		Last Modified: Wed, 20 Mar 2024 23:10:44 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3bed7de3361d2f3bce82a2de1750d8ade5521c706bd819c3615bfcfebd99ab`  
		Last Modified: Wed, 20 Mar 2024 23:10:44 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json
