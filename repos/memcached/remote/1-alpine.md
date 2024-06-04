## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json
