## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:709ca82c737ee52acc94da9623ba812e9117074d754b5aa2060faae09e9cae75
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

### `memcached:alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json
