## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:4fb13e4757387000230be124c5a74f107abfd1f65e2526f4c627110d666bf5a3
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

### `memcached:1-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json
