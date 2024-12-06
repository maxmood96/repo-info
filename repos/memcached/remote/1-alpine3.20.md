## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; riscv64

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

### `memcached:1-alpine3.20` - unknown; unknown

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

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json
