## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:19d0005f355b172894f82ef438cbd84f190e3c1198c31b4d2116619b40b13f3d
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json
