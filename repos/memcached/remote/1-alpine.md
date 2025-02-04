## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

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

### `memcached:1-alpine` - unknown; unknown

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

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json
