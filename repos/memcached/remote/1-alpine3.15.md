## `memcached:1-alpine3.15`

```console
$ docker pull memcached@sha256:06bc630f006be575ae4e8a55e515a66daba0ed432f0e46ecfacf654daf4f07e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.15` - linux; amd64

```console
$ docker pull memcached@sha256:fbb3eda59b2f6851b1335f6fd43fa5a371ac197b06f84c0363341b7cd1c066f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3864898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcea36e93e267587df645dc2c39d08513419e129eb5b28db4a204207d64a9ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:54:14 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 05 Apr 2022 09:54:15 GMT
RUN apk add --no-cache libsasl
# Tue, 05 Apr 2022 09:54:15 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 05 Apr 2022 09:54:15 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 05 Apr 2022 09:57:57 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 05 Apr 2022 09:57:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 05 Apr 2022 09:57:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Apr 2022 09:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 09:57:58 GMT
USER memcache
# Tue, 05 Apr 2022 09:57:58 GMT
EXPOSE 11211
# Tue, 05 Apr 2022 09:57:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c437462196847904d5021a85f817fecbb0b84eca04e4677f3a907f95125ebd3`  
		Last Modified: Tue, 05 Apr 2022 09:58:27 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37749f62d258e02c4f026b7ed0cb874d23b47abaa2c5860e41b3c099fdeb1d15`  
		Last Modified: Tue, 05 Apr 2022 09:58:27 GMT  
		Size: 109.2 KB (109172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf6c1e9f5167a143f222aea98c5b9c1d58ad0f9eed19d753fa1c4ffdfdd0269`  
		Last Modified: Tue, 05 Apr 2022 09:58:27 GMT  
		Size: 939.5 KB (939497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550e19164877083e509bb0c014a831674a7b77ddcf111d980a4f2b1bd1a78171`  
		Last Modified: Tue, 05 Apr 2022 09:58:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515f37e9ad844fe3fdd82c3504b1c092e11e2c8f5f8395bc8944c96c768f3d3c`  
		Last Modified: Tue, 05 Apr 2022 09:58:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d38012edd86b9a7abab01b390d4bbce8c39201ebedfd0066fcff6b6fb20cf178
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0f3d4ef24801f58b76d5d0e24224de96c6e02fba4eccb3fa2e037e94403f0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:15:56 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 05 Apr 2022 04:15:57 GMT
RUN apk add --no-cache libsasl
# Tue, 05 Apr 2022 04:15:58 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 05 Apr 2022 04:15:59 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 05 Apr 2022 04:18:36 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 05 Apr 2022 04:18:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 05 Apr 2022 04:18:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Apr 2022 04:18:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 04:18:39 GMT
USER memcache
# Tue, 05 Apr 2022 04:18:40 GMT
EXPOSE 11211
# Tue, 05 Apr 2022 04:18:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa012cdcd391bd8cd78796fe53eb96b7585962832b802667f44cedd88405d0cc`  
		Last Modified: Tue, 05 Apr 2022 04:19:28 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca8ad568702372595d83e4a4b906e000230b00315e1fd6ef6d219697badb387`  
		Last Modified: Tue, 05 Apr 2022 04:19:28 GMT  
		Size: 110.5 KB (110499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ae8d237ddc109ffe7e544e93a0dc1cea5bfe3fa5685fca792afda6d67ed0f`  
		Last Modified: Tue, 05 Apr 2022 04:19:29 GMT  
		Size: 928.4 KB (928406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce17e42e65242140f2a8f7c6d0a16bf4f1b64b0ba276ed8341905ed6f63e4a7b`  
		Last Modified: Tue, 05 Apr 2022 04:19:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30070b7f5a7be9b35fb6b8c7f1b6cb0de4508d927cc49caf12b3f6e220b0cc60`  
		Last Modified: Tue, 05 Apr 2022 04:19:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.15` - linux; 386

```console
$ docker pull memcached@sha256:5378334a3366058f6987024a1963dceafda46b182d6236b4685f816238f99992
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3888728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d8aa97e2099f400479214a98c34c3a23c21939afde5c6611961b33539a8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:52:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 05 Apr 2022 03:52:18 GMT
RUN apk add --no-cache libsasl
# Tue, 05 Apr 2022 03:52:19 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 05 Apr 2022 03:52:20 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 05 Apr 2022 03:55:15 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 05 Apr 2022 03:55:17 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 05 Apr 2022 03:55:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Apr 2022 03:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 03:55:19 GMT
USER memcache
# Tue, 05 Apr 2022 03:55:20 GMT
EXPOSE 11211
# Tue, 05 Apr 2022 03:55:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cddc8f8c3aabebd92d18ccbc0c9181ed94cc4b15b5adbda9e2bfdf4b8f38e9`  
		Last Modified: Tue, 05 Apr 2022 03:56:08 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8594347186db0e9366f74b1e03bd14ed234378b2d1238a6b56504a86608fa6`  
		Last Modified: Tue, 05 Apr 2022 03:56:08 GMT  
		Size: 120.9 KB (120869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d7907ab18015191139b22c9b7b25c6a23d1c569470a49f2eb3e1ef985c4450`  
		Last Modified: Tue, 05 Apr 2022 03:56:08 GMT  
		Size: 947.2 KB (947242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d6dff2eb04a8a959a2e8d101ca3da2646db4b2125b02fd6505c61ce53215b`  
		Last Modified: Tue, 05 Apr 2022 03:56:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845b50269336006037a46780211bf0b2b95df971864d348d10c893aa2bf3afe3`  
		Last Modified: Tue, 05 Apr 2022 03:56:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.15` - linux; ppc64le

```console
$ docker pull memcached@sha256:d1110704ee41f1dce802400ce09904c39aff25c66c1e1b87c64781b0bd9527d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1827e9495120e553b560bd77e162a97bfdb923a96c36b2dea8afd967fdc57bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:09:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 05 Apr 2022 10:09:31 GMT
RUN apk add --no-cache libsasl
# Tue, 05 Apr 2022 10:09:35 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 05 Apr 2022 10:09:41 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 05 Apr 2022 10:12:56 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 05 Apr 2022 10:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:13:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Apr 2022 10:13:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 10:13:10 GMT
USER memcache
# Tue, 05 Apr 2022 10:13:12 GMT
EXPOSE 11211
# Tue, 05 Apr 2022 10:13:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8124818eb8eba84f8929c5e21fa177a0224a632a260382b31fd9ea53de0cb63`  
		Last Modified: Tue, 05 Apr 2022 10:14:09 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65727b8884a0072f667d76a190572aecbef43ea2013aa1fab131f8ad94cf6027`  
		Last Modified: Tue, 05 Apr 2022 10:14:09 GMT  
		Size: 126.2 KB (126153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdd85c6abf5a16922e7e67ae0f58814880550c8e561aa25fe98f824c65e283f`  
		Last Modified: Tue, 05 Apr 2022 10:14:09 GMT  
		Size: 966.1 KB (966088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72641c2cb945038b7f950ba927f9377d909670cd2c8a2f99f0027cfe6f34d41f`  
		Last Modified: Tue, 05 Apr 2022 10:14:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27047ea6a5173f1f7f40a46c10833cfbf360f9ac71f5595dd2b745afc3f9f3bb`  
		Last Modified: Tue, 05 Apr 2022 10:14:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.15` - linux; s390x

```console
$ docker pull memcached@sha256:f4d6b61f33632664a2176b827e6f04dc9b43bece1e1225f1c27d3f218fcaf90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d81b27c0ae4d75825efc6c14a9b31769a43cebc314ab07e25b9024fe3b7d6bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:18:54 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 05 Apr 2022 11:18:55 GMT
RUN apk add --no-cache libsasl
# Tue, 05 Apr 2022 11:18:55 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 05 Apr 2022 11:18:55 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 05 Apr 2022 11:22:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 05 Apr 2022 11:22:16 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:22:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Apr 2022 11:22:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:22:17 GMT
USER memcache
# Tue, 05 Apr 2022 11:22:17 GMT
EXPOSE 11211
# Tue, 05 Apr 2022 11:22:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d92848f08937ad9e3c8df84e91a6ae677af747e7ae736062bf8303e6f98a5a`  
		Last Modified: Tue, 05 Apr 2022 11:23:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4699d5d9185c820000eb9490520b6c45f7c7df9e07c67d79ec6efac05ff170`  
		Last Modified: Tue, 05 Apr 2022 11:23:08 GMT  
		Size: 113.5 KB (113464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c834b41bef6837d1312846d4839e66a0070dd934cb4388ff09a93112f6cdc0`  
		Last Modified: Tue, 05 Apr 2022 11:23:09 GMT  
		Size: 934.6 KB (934639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd760c99b09ff84bd3f703d93a143abd83f2ecfc7c941856bdd4222a4da2b7a`  
		Last Modified: Tue, 05 Apr 2022 11:23:08 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4795384f4f0fbaa99dd9e3683dfd3639ccbcd001144f0b8d1f050c3a765283`  
		Last Modified: Tue, 05 Apr 2022 11:23:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
