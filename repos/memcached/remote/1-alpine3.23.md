## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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

### `memcached:1-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:49:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:33:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:17 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 06:53:16 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 06:53:16 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json
