## `memcached:alpine`

```console
$ docker pull memcached@sha256:f0f3c2a07b8f5d6ffe7bebab5bd4956166b919ce83a56958a641fe2c2d5b2aa9
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
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
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
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
		Last Modified: Fri, 13 Dec 2024 16:51:49 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 16 Dec 2024 10:11:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Sun, 15 Dec 2024 20:07:21 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Sun, 15 Dec 2024 20:07:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 16 Dec 2024 08:39:05 GMT  
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
		Last Modified: Mon, 16 Dec 2024 10:11:31 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json
