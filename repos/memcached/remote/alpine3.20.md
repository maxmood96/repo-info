## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:e5abbee7becc49f8533ffe4521a38f95ef72b202c3868f81f4da1f6dc8cb888e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; 386
	-	unknown; unknown

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
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
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json
