## `memcached:1-alpine3.24`

```console
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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

### `memcached:1-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json
