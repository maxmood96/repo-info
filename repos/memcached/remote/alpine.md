## `memcached:alpine`

```console
$ docker pull memcached@sha256:7944216f8983837d1bc4ad08793beb83b3fb0870de98fde50491d63037f204bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:95b4d489fb9cda325b84ddc17c56a1d600cf3c28eaafd5a6fb81f0e3b2513973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e591ed3d0226cc7ecc9595b4df1217f509b3b205ed3d2e81f1072a9848a983c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244924c5367c4dc5fff99b915a932cc87d84194cb449f4afa934bbbef386d649`  
		Last Modified: Wed, 05 Feb 2025 20:30:22 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07a56e9186251d957d4df438f320f771cc2f444f1fec3857d04e778ca17a4ac`  
		Last Modified: Wed, 05 Feb 2025 20:30:22 GMT  
		Size: 104.7 KB (104688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1ce8ce91a0c6d064b0f39ef43ae21b3038c298d1f2f3e6f1188d688746639f`  
		Last Modified: Wed, 05 Feb 2025 20:30:22 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e583b490e2ea4ce6a92fd76c07de1d40daec81f05be5179fafb256953f3e7d`  
		Last Modified: Wed, 05 Feb 2025 20:30:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9401c2895486d5ad9e4c1abd1ecbcc17379b4d3fbff4b94e67ae9b49e6fdd8dd`  
		Last Modified: Wed, 05 Feb 2025 20:30:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd781d552952031ca7807c485f2608909f9b7e0f840a9d9e9118bbbcc00b07fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e908bb3aca83f934653518354d3528804749eee67da45ca094631ec2cbfc2942`

```dockerfile
```

-	Layers:
	-	`sha256:4a5fb7e76e3f9d06d9152abcc048ad34cedd5d3757393e274778527b39c3c259`  
		Last Modified: Wed, 05 Feb 2025 20:30:22 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4163c00ca938d9b3187b3764d8400e98a8e8ea19300c0fa86876e55892c16ed0`  
		Last Modified: Wed, 05 Feb 2025 20:30:22 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 20:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 20:34:10 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 20:34:11 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 20:34:10 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 20:34:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 20:34:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 20:34:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:ef212dbdd266d86debf56798a7375a7eb42a03ab6f4211a20895c2b2c0037810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6318dbdbd3a70fc53361397e1831d2e92d936ff871978e1e59321dc6fe6ddb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0266c4cdf6e75f7e286bafd0ec9ad2b96f9959ff44e9a89cc5dfbc50e24f9441`  
		Last Modified: Wed, 05 Feb 2025 20:30:25 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9569d97055be318069397cd73e2396998addcc1f896d9101c2715b04ff66e5`  
		Last Modified: Wed, 05 Feb 2025 20:30:25 GMT  
		Size: 109.5 KB (109462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237992bf659c8cd6b0f36e049081dddb2731c821b92b4fd53ae5a7dcab1888b6`  
		Last Modified: Wed, 05 Feb 2025 20:30:25 GMT  
		Size: 960.2 KB (960202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e950ba0755d66c44924df09c372b061c6a7668546a26918adae487eacbc855`  
		Last Modified: Wed, 05 Feb 2025 20:30:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12052101c3532399e264dbc72b22fbf682aa8436242f920460a3fd01008bf09`  
		Last Modified: Wed, 05 Feb 2025 20:30:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:14b66aae9503004991718811b375881540bd442572e7db94e4817c131c695f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06b9bf3e97f4ceedc8454edacdcbe9077487d47ddda1bf47446ef47e7a520f3`

```dockerfile
```

-	Layers:
	-	`sha256:4beaa939730c6ecb62dc02ad1bd5576f7892f7d3fa65f34f8195b6f05cdbda16`  
		Last Modified: Wed, 05 Feb 2025 20:30:25 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74e5327702ae595a2ecf04df7e1692ed60494c6ad5c7e87abb9866484ae1555`  
		Last Modified: Wed, 05 Feb 2025 20:30:25 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3513971b00f5ed181df585da849e9c57eab12e734749804c209e28f9305e2696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92330162be8bf00655353569e8c624dc8033c19d4357a497f15beed5981335eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352f886ba8d95b18b422c90b93234bd0856f9e3ef97fae58555baf8609ee0dec`  
		Last Modified: Wed, 05 Feb 2025 20:32:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15280609a7c594ab91c02757dff240103fbfe783ee94f257616f7c99b059162c`  
		Last Modified: Wed, 05 Feb 2025 20:32:26 GMT  
		Size: 124.3 KB (124281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7ffc4622d1872fa745d7cdca255913eba47494b067dccea4abae84641e75e4`  
		Last Modified: Wed, 05 Feb 2025 20:32:26 GMT  
		Size: 1.0 MB (1006819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1c8f141a330f195ccc00e23b19582a24f3bc4bfd4f02c6cec4993421458cd3`  
		Last Modified: Wed, 05 Feb 2025 20:32:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b91dae2ab2aa739a07ebacde6f3a4a30356a0a8582d54c56d5f0c754d478c`  
		Last Modified: Wed, 05 Feb 2025 20:32:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a86d07a772af536d8bf19d28aca71d99dbf636da923d58160d14c0ae817b902f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a570ea73866acaa6bb497cd79f5e9cce46726eeeca0e9bfbdb441ece140d53e7`

```dockerfile
```

-	Layers:
	-	`sha256:50e597f07cf4012e42dcffc7dad69a023b6b4403a14a4ab14aa1a639b81e6188`  
		Last Modified: Wed, 05 Feb 2025 20:32:26 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a36b8aee54e81de7def396f53a3830c274323c8dfb1c9d2d3e9932d1316864f`  
		Last Modified: Wed, 05 Feb 2025 20:32:26 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:375bc4a61dc65edd8163c937d69501c0325b5c7d7660f6974982e2d1a309997d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e392ea20bd35f4d756e6ad6715b6f827c20e0123a8ad74bac56b2122e42b76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.32
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.32.tar.gz
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a6377de830d15e17b769184df6ad20766c2279d9
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
USER memcache
# Mon, 21 Oct 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 21 Oct 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 18 Nov 2024 05:57:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73411748d41c8900a2e46b2e84cda57890db94ff010e5767e7d503fb301c5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434574b080a33771844da9fe1f65ae99a8060f103229f83485f9b276ccbf830b`

```dockerfile
```

-	Layers:
	-	`sha256:1282c9de70eafb095b4d790a1e60386966df96e786c3e1acb71c18a762e42b04`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:9dfe26d0e3cc996c79c0e7488a271710f3d244603f1f67e1147aa6dcd627da26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfc77be2c8db9f4a7d69238f2347e8fdb8f34df62504c50fe549291fafb45ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24444ed241b9152e096e61c59b4f8678291ff1e8cb852bcef0383413eae777e7`  
		Last Modified: Wed, 05 Feb 2025 20:35:59 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2529a3c18c5ad29da69c1b03819dcfc2409948c417e8af6d6d15a699b33585`  
		Last Modified: Wed, 05 Feb 2025 20:35:59 GMT  
		Size: 113.5 KB (113453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fa28d27956f72bfff12c427e698cd55c44a106fec0f359db733b924971e88f`  
		Last Modified: Wed, 05 Feb 2025 20:35:59 GMT  
		Size: 988.6 KB (988619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c501f40d3216f856dda874b56d648ba305b2204fef0f6113a4be4956dcf2c45`  
		Last Modified: Wed, 05 Feb 2025 20:35:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f72e2f631b9dd085c47e6e2c4250ec9ee3603db35fc38e1ae1435bdffb09f`  
		Last Modified: Wed, 05 Feb 2025 20:36:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c17331b891512c1ee1b1dab5ec95dec89494c9280f2aa002368f32f465627b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b370c7b2d2cd96cf2f543bf4e9f81f11d4c6a34b9d58c3c1eb2d5f25c192fa88`

```dockerfile
```

-	Layers:
	-	`sha256:8f194f20f09ad3678415934f0bdb2f4cae83ff1d1d7feca1c0219fb084bedeaf`  
		Last Modified: Wed, 05 Feb 2025 20:35:59 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e3619920b9bdc66010fc183a0657f58e5b2ddce1ec32c654715e0bbb91cf78`  
		Last Modified: Wed, 05 Feb 2025 20:35:59 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json
