## `memcached:1-alpine3.13`

```console
$ docker pull memcached@sha256:c3e83faa6cafa443fe8e10e9773a25daf7127ccc325962d8cfd55792c903c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.13` - linux; amd64

```console
$ docker pull memcached@sha256:e2e06014861fa2fa0cda5e2c23d0fc1d62d84337fe214ab73ca71a5a444871e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b141d8b3010e5ed0812b45e69e6572b00994f4948d106ea1d9cb6bae5d5a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:08:14 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Apr 2021 23:08:15 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Apr 2021 23:08:15 GMT
ENV MEMCACHED_VERSION=1.6.9
# Wed, 14 Apr 2021 23:08:16 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Wed, 14 Apr 2021 23:12:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Apr 2021 23:12:12 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Apr 2021 23:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Apr 2021 23:12:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:12:13 GMT
USER memcache
# Wed, 14 Apr 2021 23:12:13 GMT
EXPOSE 11211
# Wed, 14 Apr 2021 23:12:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c59c3d3514e5e7882bf45c670360abc6ddf52dd8cc8726167f2fbb8a615a9`  
		Last Modified: Wed, 14 Apr 2021 23:12:37 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ed50ac5963e439913b39f5b30752d318c76f1f1fd5c007a904b522d90dc1fe`  
		Last Modified: Wed, 14 Apr 2021 23:12:37 GMT  
		Size: 155.2 KB (155229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5f84fa6eb54d5eb8a48e0a80620c4acd312918bf7c2dccff78f1dd5af87086`  
		Last Modified: Wed, 14 Apr 2021 23:12:38 GMT  
		Size: 867.3 KB (867338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41105c4de6bd490f07b56713ee7e56e282be54d144b453a75abd1e6a3b8cd95`  
		Last Modified: Wed, 14 Apr 2021 23:12:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c886a0dc42a09e2eff365af2952edb0b2f390e63fd9c234ba52395346e74e40f`  
		Last Modified: Wed, 14 Apr 2021 23:12:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:401e9435b87a5a8b3aa0e513ce16e622b4199e3571ecde4cc81cbb98beaa485c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44bbd9089735cadb559379e745be2d730474571cd037c47f831dcc3f373a9af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 00:58:24 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 16 Jun 2021 00:58:25 GMT
RUN apk add --no-cache libsasl
# Wed, 16 Jun 2021 00:58:25 GMT
ENV MEMCACHED_VERSION=1.6.9
# Wed, 16 Jun 2021 00:58:26 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Wed, 16 Jun 2021 01:02:23 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 16 Jun 2021 01:02:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 16 Jun 2021 01:02:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 16 Jun 2021 01:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:02:24 GMT
USER memcache
# Wed, 16 Jun 2021 01:02:24 GMT
EXPOSE 11211
# Wed, 16 Jun 2021 01:02:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31c94f151b46633317aeda8c2696b35e4da82f944b368fb7447c8add9624660`  
		Last Modified: Wed, 16 Jun 2021 01:03:17 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df71ba737b9de9eacbdf1a8eacaad61a6c799f84861cf8afe72e7d75c81987b3`  
		Last Modified: Wed, 16 Jun 2021 01:03:17 GMT  
		Size: 157.4 KB (157360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bcaa83494be4b3984d2a691c0bb58f8484795da6670e9fa2ac1332d7deab0d`  
		Last Modified: Wed, 16 Jun 2021 01:03:17 GMT  
		Size: 1.3 MB (1252779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8c469f334727e2da2a1b18b60c6d854485b8b3863fed04b9de9825c7de2fc`  
		Last Modified: Wed, 16 Jun 2021 01:03:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347a3b1748a923250555c86f515efa2a7286e4322b87d9d3a7fdd06bd24a836b`  
		Last Modified: Wed, 16 Jun 2021 01:03:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.13` - linux; 386

```console
$ docker pull memcached@sha256:c88904c9a172c1801d6789b6d029d5406d4438f3e0c90d7a656d4831bd1f443c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6950b4b9c574e57f6980e5c9ab9729de9f94704d82225e4706c165c4e26ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:09:20 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 15 Apr 2021 02:09:22 GMT
RUN apk add --no-cache libsasl
# Thu, 15 Apr 2021 02:09:22 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 15 Apr 2021 02:09:22 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 15 Apr 2021 02:13:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 15 Apr 2021 02:13:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:13:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 15 Apr 2021 02:13:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:13:56 GMT
USER memcache
# Thu, 15 Apr 2021 02:13:56 GMT
EXPOSE 11211
# Thu, 15 Apr 2021 02:13:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd56a31f106d1c60e7a8badb73a603a32f064afd704ec619653bca95378f8e4`  
		Last Modified: Thu, 15 Apr 2021 02:14:39 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5c2c0e1078af1eae54b4aaa4a62149c3dc46ac8ef32d44726f65921598692d`  
		Last Modified: Thu, 15 Apr 2021 02:14:39 GMT  
		Size: 168.7 KB (168716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0165a5dae48239662502d69cb7dbefd3d9102bf3a7c4c310bdde4e179e06985b`  
		Last Modified: Thu, 15 Apr 2021 02:14:40 GMT  
		Size: 878.7 KB (878724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c4c70b95d11ee36c207e4da297466eb6eba0669737d5d549e6be374599954d`  
		Last Modified: Thu, 15 Apr 2021 02:14:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b74225946c8fb4940ef6171292ab277b64193d612247a241f21e13ec68ab4e4`  
		Last Modified: Thu, 15 Apr 2021 02:14:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.13` - linux; ppc64le

```console
$ docker pull memcached@sha256:9fea9a6cc1760904837d9150f67df80b031982be8c10e3b10fb8cb804703f196
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4282059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55225bb4e3c772e83b598d3e0fd57904e2e37c37e0d9c1ca2ca81ec70dceb0a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Mon, 12 Jul 2021 22:18:56 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 12 Jul 2021 22:19:14 GMT
RUN apk add --no-cache libsasl
# Mon, 12 Jul 2021 22:19:19 GMT
ENV MEMCACHED_VERSION=1.6.9
# Mon, 12 Jul 2021 22:19:24 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Mon, 12 Jul 2021 22:23:02 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 12 Jul 2021 22:23:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 12 Jul 2021 22:23:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 12 Jul 2021 22:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Jul 2021 22:23:28 GMT
USER memcache
# Mon, 12 Jul 2021 22:23:34 GMT
EXPOSE 11211
# Mon, 12 Jul 2021 22:23:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246272a394d33197cbeeba72fd51e92fd0cd5329fdf484384ade42e5bf898403`  
		Last Modified: Mon, 12 Jul 2021 22:24:34 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15397f165a719894617ab5d2d19eef1e11da0ceb4ff54b1aac2f6217adaee7da`  
		Last Modified: Mon, 12 Jul 2021 22:24:34 GMT  
		Size: 179.4 KB (179426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ac4fb457c361858bf2bc038f05f5dbc152192d55a0363bd2a6d7640156f57d`  
		Last Modified: Mon, 12 Jul 2021 22:24:34 GMT  
		Size: 1.3 MB (1287827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf921adafb6294a56ec0ba0b136d23efbc612c9661cd3a0be14dd7afe54f4ca`  
		Last Modified: Mon, 12 Jul 2021 22:24:34 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635287102033375bf9f03d8c75b11fb1e645627ebcb2bfe2e0a0f7dfcc2375d6`  
		Last Modified: Mon, 12 Jul 2021 22:24:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.13` - linux; s390x

```console
$ docker pull memcached@sha256:e0252fb6b60c078fe7430214980295ba5bb0b9a2cf48b7bf4984b5263f62e4d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f8e2770b3b8d803505b284b76724c9e251cc86cb451c857c10b969dbe2afca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Mon, 12 Jul 2021 22:42:52 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 12 Jul 2021 22:42:54 GMT
RUN apk add --no-cache libsasl
# Mon, 12 Jul 2021 22:42:55 GMT
ENV MEMCACHED_VERSION=1.6.9
# Mon, 12 Jul 2021 22:42:55 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Mon, 12 Jul 2021 22:46:53 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 12 Jul 2021 22:46:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 12 Jul 2021 22:46:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 12 Jul 2021 22:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Jul 2021 22:46:56 GMT
USER memcache
# Mon, 12 Jul 2021 22:46:56 GMT
EXPOSE 11211
# Mon, 12 Jul 2021 22:46:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108a508c6c5b4a3ea3bf48376a710002cbc420f1b55e8666938db6f9bed5794`  
		Last Modified: Mon, 12 Jul 2021 22:47:53 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9194724c2d27d4c00fd6de0de7609e0d17a2c02741d7b194c85a1c327f5e1d`  
		Last Modified: Mon, 12 Jul 2021 22:47:53 GMT  
		Size: 161.2 KB (161200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb98e038290933dc63c75726fac9389b7976671266608c39ac026f73c9cea776`  
		Last Modified: Mon, 12 Jul 2021 22:47:53 GMT  
		Size: 1.3 MB (1261703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da85c00a2d21aa62b2a0cd4b7b3599ef39ebff34d84eb0caf3f95c38b3a4912c`  
		Last Modified: Mon, 12 Jul 2021 22:47:53 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330bfd66f8c196098e10f1d155f7394aef83f15d9c4e21bbc2acc04c1558aa3`  
		Last Modified: Mon, 12 Jul 2021 22:47:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
