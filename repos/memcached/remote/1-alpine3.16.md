## `memcached:1-alpine3.16`

```console
$ docker pull memcached@sha256:266b99ed5477a6ea69353f32a7f1e51387b7968ddd9d8d560f100ef82159b554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.16` - linux; amd64

```console
$ docker pull memcached@sha256:9b2ecb3fb8713d7c971eaf6e97150fcf34735d105bab81dd53e45d18da6c6b90
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e40b7fd940b01ddffc7c8fddff80d89c6572d89d7c9664343a2c1e3efe389b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 01:33:13 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 19 Jul 2022 01:33:14 GMT
RUN apk add --no-cache libsasl
# Thu, 04 Aug 2022 20:02:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:02:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:05:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 04 Aug 2022 20:05:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:05:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:05:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:05:10 GMT
USER memcache
# Thu, 04 Aug 2022 20:05:10 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:05:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e13ff258fbd16cc42fcdb1bd800f73f4b380857d2a6096906444ec790c6542`  
		Last Modified: Tue, 19 Jul 2022 01:36:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90922b6720c8f20007711c5660b8269518b50979be1cef2cb4c0b12a7ac78ff7`  
		Last Modified: Tue, 19 Jul 2022 01:36:41 GMT  
		Size: 108.3 KB (108315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa27d6f4905ed1e531c58fa8d22676bfac86a2ba49c01894f95245d65329f7`  
		Last Modified: Thu, 04 Aug 2022 20:06:10 GMT  
		Size: 951.4 KB (951422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e3d85200a71563435aa4bb45d98232f964b19c4facc2bc63d6ae3db816cbb4`  
		Last Modified: Thu, 04 Aug 2022 20:06:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba9b8d8a47b35ef57b45387b27d98410a32a2814a83a6cc686136b48fbb420`  
		Last Modified: Thu, 04 Aug 2022 20:06:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc07b144753a49e0df4c460d54f8ca71f1b32e7e342bdeda073a6d07959d1fc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b0ac8e073d1285f1616cf2c260d108c87a889247e1d41af425b873498b2656`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:40:46 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 18 Jul 2022 23:40:48 GMT
RUN apk add --no-cache libsasl
# Mon, 18 Jul 2022 23:40:48 GMT
ENV MEMCACHED_VERSION=1.6.15
# Mon, 18 Jul 2022 23:40:49 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Mon, 18 Jul 2022 23:43:31 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 18 Jul 2022 23:43:32 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 18 Jul 2022 23:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Jul 2022 23:43:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 23:43:34 GMT
USER memcache
# Mon, 18 Jul 2022 23:43:35 GMT
EXPOSE 11211
# Mon, 18 Jul 2022 23:43:36 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da60570c25aa47c5a2b9fcd4be47a0a93240f9f4f2ab5a4d0b52c2646f40a28`  
		Last Modified: Mon, 18 Jul 2022 23:44:19 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a722c1c0875bed8b5bc87f4e2844ed10d7d9c12755721cd2164aa8b1c690d3`  
		Last Modified: Mon, 18 Jul 2022 23:44:20 GMT  
		Size: 109.6 KB (109554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35806132458f95287ff0e7cf4297c49240c8c4b485aebb817052bebc5f50ba`  
		Last Modified: Mon, 18 Jul 2022 23:44:20 GMT  
		Size: 931.5 KB (931493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914c3251c7e3d100d3eb8855064c1fb24c72a0897b6a09b7ca11c3d852f3c8e3`  
		Last Modified: Mon, 18 Jul 2022 23:44:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2018358fc9c8d987b80e1b8b4b6ed865fbf7eea88f27ec778f2e58104aef686b`  
		Last Modified: Mon, 18 Jul 2022 23:44:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; 386

```console
$ docker pull memcached@sha256:7ce1fc4d0379d8dc70a3dba9c276bfb6d26f025330a139f05ecf2ee650e45e9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3878850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89f790aead4ae48532815197fbcf96e226d9c34e4e2f56d0bca603feb0894f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 01:27:41 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 19 Jul 2022 01:27:42 GMT
RUN apk add --no-cache libsasl
# Tue, 19 Jul 2022 01:27:43 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 19 Jul 2022 01:27:44 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 19 Jul 2022 01:30:33 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 19 Jul 2022 01:30:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 19 Jul 2022 01:30:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 19 Jul 2022 01:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 01:30:37 GMT
USER memcache
# Tue, 19 Jul 2022 01:30:38 GMT
EXPOSE 11211
# Tue, 19 Jul 2022 01:30:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd21aea877c073ddb40c30afa2f3e8f58c6fef7737835158747cf175df4ef4e`  
		Last Modified: Tue, 19 Jul 2022 01:31:30 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba37b4bd3e4b8bdb4184c8f065ce7b15f3fadd48bbb46f43623a90737e59911`  
		Last Modified: Tue, 19 Jul 2022 01:31:31 GMT  
		Size: 119.8 KB (119833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb5bddad19c0b8b20d9d2bb147ab8e9f40390a11791aa01d04bebc4adc9c31`  
		Last Modified: Tue, 19 Jul 2022 01:31:31 GMT  
		Size: 955.0 KB (955038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f30230d3a7cab24e8ce67e6e4adf648aa885e090bfa5d30e42a930cc8e16b`  
		Last Modified: Tue, 19 Jul 2022 01:31:30 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78c3ae988f057ce783950b95abffb2a5f2d1a63ad424909f54b1950204a2e6c`  
		Last Modified: Tue, 19 Jul 2022 01:31:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:71acafc285acbf979e4da67a2eec4b418146053e89aa969cb816a25d360b2c8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3898528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576638982440cbe02392fd4b93eb2a91f8518c8644faf7f14c217994d369bbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Aug 2022 03:48:55 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 02 Aug 2022 03:48:57 GMT
RUN apk add --no-cache libsasl
# Tue, 02 Aug 2022 03:48:57 GMT
ENV MEMCACHED_VERSION=1.6.15
# Tue, 02 Aug 2022 03:48:58 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Tue, 02 Aug 2022 03:52:15 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 02 Aug 2022 03:52:15 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 02 Aug 2022 03:52:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 03:52:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 03:52:17 GMT
USER memcache
# Tue, 02 Aug 2022 03:52:17 GMT
EXPOSE 11211
# Tue, 02 Aug 2022 03:52:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6cec9872fd3c66c2b19cff2dd853136a16b03e523f70d0cd8875dff75abdf6`  
		Last Modified: Tue, 02 Aug 2022 03:53:48 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2420696d84e23c3f6e09fb61166d22a8b83d011559aa421d5d5e9f4ccf2f06a`  
		Last Modified: Tue, 02 Aug 2022 03:53:48 GMT  
		Size: 126.1 KB (126059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0baf84bb4d210e435da081e92263789fc1e6d088cc1a578b95fd1848505eab0`  
		Last Modified: Tue, 02 Aug 2022 03:53:48 GMT  
		Size: 980.9 KB (980873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0802bd5e0cf3a7bd486338bcd35ade2057c3f25fd966ee55d27becd1d3f98e`  
		Last Modified: Tue, 02 Aug 2022 03:53:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c400863d0336848ad73fbbdac59da65e2cb38f1327eeaa58b02dc0834a9e8f1b`  
		Last Modified: Tue, 02 Aug 2022 03:53:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; s390x

```console
$ docker pull memcached@sha256:df751eb1a98cd8834e4c727ccae61ed6e9bfa1e513437e1f3316862d6130f02f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8a3b5b435e2ca4f3ccd1b01215a57268df90315fdea1ffe762f31a382fde33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:46:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 18 Jul 2022 22:46:46 GMT
RUN apk add --no-cache libsasl
# Mon, 18 Jul 2022 22:46:47 GMT
ENV MEMCACHED_VERSION=1.6.15
# Mon, 18 Jul 2022 22:46:48 GMT
ENV MEMCACHED_SHA1=badcfa0d65f5797cc9c2f957f3fbfedbd8c13411
# Mon, 18 Jul 2022 22:51:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 18 Jul 2022 22:51:31 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:51:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Jul 2022 22:51:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:51:35 GMT
USER memcache
# Mon, 18 Jul 2022 22:51:36 GMT
EXPOSE 11211
# Mon, 18 Jul 2022 22:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b6f46f9ccd4c19bfc103544d0d83ceef7feae4d70d25397d620ca381065659`  
		Last Modified: Mon, 18 Jul 2022 22:52:40 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f491a581763941ae0ec0ec035bdfb8073504d7fdc2eec6eb1e70878f26c16351`  
		Last Modified: Mon, 18 Jul 2022 22:52:40 GMT  
		Size: 112.5 KB (112503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b6ffa9d3eff258d85a3d3cdbb3d85024bca8dacf18d278924e20f243b2d39b`  
		Last Modified: Mon, 18 Jul 2022 22:52:40 GMT  
		Size: 934.6 KB (934636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571fb3eedfc09b0b915c7cfeeb025e8b7c586dce0deb34613d640c98f1acc62`  
		Last Modified: Mon, 18 Jul 2022 22:52:41 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7ae80e50a8d57ec32d7e37083377d2e89c9b11da47e54b02dde318a4ae1a99`  
		Last Modified: Mon, 18 Jul 2022 22:52:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
