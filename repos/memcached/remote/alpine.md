## `memcached:alpine`

```console
$ docker pull memcached@sha256:dbf2bd76d19ae458150cef4f67a479fab425a08021ac454dcc6372a94c1fc39e
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json
