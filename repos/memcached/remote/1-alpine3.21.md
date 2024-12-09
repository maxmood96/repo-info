## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:d616f6d2bcf78936578bbc503240fabc43ae6467b364ed08e3f937cfb5a12c6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `memcached:1-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:156bc025f995df7b7c19427fa4ce940b4f03d4f730c42426ec495848a588e5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4714459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9919ef9d10b8ffeeab45707d9ce1b7941a500c96b0503b2ac3ccfa80dc9c24b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fc126b3aab3b781996481e696cc68a93d7cfbc571290f2c55cc441f805fba6`  
		Last Modified: Mon, 09 Dec 2024 20:33:03 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7983e46fab3e9c8efd764578f4a59a4e576992915df9e66532feed8c91761f82`  
		Last Modified: Mon, 09 Dec 2024 20:33:04 GMT  
		Size: 104.7 KB (104680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07db05dcedb5293629a535a6be9161df8064dcbe9fb2c45207fc13f326f75682`  
		Last Modified: Mon, 09 Dec 2024 20:33:04 GMT  
		Size: 964.0 KB (963977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644b87165cb6624e9f94d077b49eab6d6dc00b848da45af91e9c45fcda72a1f`  
		Last Modified: Mon, 09 Dec 2024 20:33:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61d31fb1e0ba101693f22ab727ff4f2ef7fe3efd3b413ab46a33ee0bda09db7`  
		Last Modified: Mon, 09 Dec 2024 20:33:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:5c0a0d8c3bd7f7ce87dbca52c12a340e84cd34c73c1869a8bf8cd8d8f2e47043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 KB (113295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f58e4861cf455b44e3bf17eabb846bf3a0b0095f400e1a45f07b12ee692fe2`

```dockerfile
```

-	Layers:
	-	`sha256:ea5a154f0475c5ed491e777c3c9718158bf2ef8c3ae83622379bff761a720515`  
		Last Modified: Mon, 09 Dec 2024 20:33:04 GMT  
		Size: 93.7 KB (93724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2efc822a0431bc91ac96421e034ae39cfe05b5c4fffa4c8bb9105026b7318f`  
		Last Modified: Mon, 09 Dec 2024 20:33:04 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6263c127197a1481b125b0286bfc4d5e1f64c5813a4e96d6d9e92f838e8de116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced2d2195542b8b79a4ce9b7aab80cea4176461b5c673ca4385b60ba503a1994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5411233001939fe5f70e1830c30d2229c027052a8e8976a61d3854d789faa7`  
		Last Modified: Mon, 09 Dec 2024 21:02:37 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a5dcb591a584b3d61f7e849d7ee3ff102e93ffa2dfdafe328841343e58550`  
		Last Modified: Mon, 09 Dec 2024 21:02:37 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea06b6ef2f64d2fb9f529df6cebc492811ee16a82ac4947913792be55b3ca80`  
		Last Modified: Mon, 09 Dec 2024 21:02:37 GMT  
		Size: 963.8 KB (963757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644a4337d2f67a0c1a46f3c89aa8cc8e5e4861dae88f46609d179fa5cef5a52e`  
		Last Modified: Mon, 09 Dec 2024 21:02:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0596235a45d69132127bcafeae3ed29e77b2367b820b02fdb8d8b5861cab0d1`  
		Last Modified: Mon, 09 Dec 2024 21:02:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:eb29153ac09fb134f485fee4f8626498a701c52ef68f1865b8a0e1771c9118b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 KB (113596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11be0dde83098d1311c0a759da33640b05dc7cd01907fa5b492d1ad8ba45887`

```dockerfile
```

-	Layers:
	-	`sha256:d451fbb4e606e0792c64e16ea6a6f53ef6414f3104208edfff4dd6b0b5273df1`  
		Last Modified: Mon, 09 Dec 2024 21:02:37 GMT  
		Size: 93.8 KB (93828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f5453bb47cf952e14c9d819d3eaec08ceb4b11133136b2a8c4bbb30d03bee5`  
		Last Modified: Mon, 09 Dec 2024 21:02:37 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:98cb484aaa7b840bb7a8dc512ab806131ba8e22e66b0341ac86d0aaf73af1820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4533844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538258523ccf9e8cff48f33906e35af2ed2576cd3139ae284e69347a18189cc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea28da4a60156df40a3ca5774243e786c6e4c834e61157532ace84321884953`  
		Last Modified: Mon, 09 Dec 2024 20:33:44 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff8072fc7e79692827f76668ce954277e7e3b472e5e5267943f2f720005a5b4`  
		Last Modified: Mon, 09 Dec 2024 20:33:44 GMT  
		Size: 109.5 KB (109455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebda1916c6ff809967ed3c319c5a24e38210b5615a4ca9fdffb5cb9e5418aaaf`  
		Last Modified: Mon, 09 Dec 2024 20:33:44 GMT  
		Size: 956.9 KB (956944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be24a4f1678c4f5300693b582bfb6be8f6797360694a5ebd0c0611f5529a7577`  
		Last Modified: Mon, 09 Dec 2024 20:33:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5322d1899ac103502493742504c6b8ba8f8ff7825a3821cbeed8fa54e58e1`  
		Last Modified: Mon, 09 Dec 2024 20:33:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a34a0378a36314053934c672d19d99011803671ac9058805d211445df7d5310a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f10b9ded1be95bc14eefbd37aaa3ada4bb009f0f10a448a683c13f5f066907`

```dockerfile
```

-	Layers:
	-	`sha256:bafdb96aa5bd76be49ac514f89d481b3ef0ac4bd06aeb1efef1dc5534030e02d`  
		Last Modified: Mon, 09 Dec 2024 20:33:44 GMT  
		Size: 93.7 KB (93679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e5a3636c25d6414ee6fc100c70456aa7fe0b06cd9244019415a83893138407`  
		Last Modified: Mon, 09 Dec 2024 20:33:44 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json
