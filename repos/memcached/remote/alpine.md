## `memcached:alpine`

```console
$ docker pull memcached@sha256:649541d327273c8057e25948fd2fc76434a1a7639aaabdfd777d114a3a6826ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a9572bc9c9ffa766a8bd36b2d3ecd69fd5f9fffa506619c1f7a5886250740019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6144153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7fbd7ed049c5209b176ee222f7d44d78f817e2925543cff52dcd64c2dbb530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061e00fe02a58855ebe9df110e8f1605a116ee757a07f795d71f55729066bbd`  
		Last Modified: Thu, 11 Jan 2024 01:28:43 GMT  
		Size: 2.8 MB (2787034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61e5c902294ab1e7509374759fd14ec826600b3e615b10c8d9f28d515360b74`  
		Last Modified: Thu, 11 Jan 2024 01:28:43 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3bfdcaf03273460e9a1e994a758327fa9c2928fe77f5ce6143e1aeaa9d0bc`  
		Last Modified: Thu, 11 Jan 2024 01:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:16f7510594399ea35911a3bae7cf8e5432b94caa4d4b01f5828a39b20915f69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a371c3f419be550951292ef5e23a08e2f838894ba866e32c756ab016bccb0419`

```dockerfile
```

-	Layers:
	-	`sha256:bec96aca9ab51d406ee7d7d7aed88b4d4095dae0d92d6b76262ea8931ff319d0`  
		Last Modified: Thu, 11 Jan 2024 01:28:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4251a759acb0411fcc1a3890ea990e81d56c9e3487851483b4496d10a18bee`  
		Last Modified: Thu, 11 Jan 2024 01:28:43 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json
