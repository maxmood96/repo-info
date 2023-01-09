<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.17`](#memcached1-alpine317)
-	[`memcached:1-bullseye`](#memcached1-bullseye)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.17`](#memcached16-alpine317)
-	[`memcached:1.6-bullseye`](#memcached16-bullseye)
-	[`memcached:1.6.17`](#memcached1617)
-	[`memcached:1.6.17-alpine`](#memcached1617-alpine)
-	[`memcached:1.6.17-alpine3.17`](#memcached1617-alpine317)
-	[`memcached:1.6.17-bullseye`](#memcached1617-bullseye)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.17`](#memcachedalpine317)
-	[`memcached:bullseye`](#memcachedbullseye)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:4329a441c8103b0542351e1ae387f43b06d99d03a78b6d680828fda55ed7a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v7

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

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine3.17`

```console
$ docker pull memcached@sha256:782343532db9f550c030b4c87406a5e31f96a4879e2adc6dcdca0fb9d932070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.17` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.17` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.17` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.17` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-bullseye`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:4329a441c8103b0542351e1ae387f43b06d99d03a78b6d680828fda55ed7a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v7

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

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine3.17`

```console
$ docker pull memcached@sha256:782343532db9f550c030b4c87406a5e31f96a4879e2adc6dcdca0fb9d932070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-alpine3.17` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.17` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.17` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.17` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-bullseye`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.17`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.17` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.17-alpine`

```console
$ docker pull memcached@sha256:782343532db9f550c030b4c87406a5e31f96a4879e2adc6dcdca0fb9d932070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.17-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.17-alpine3.17`

```console
$ docker pull memcached@sha256:782343532db9f550c030b4c87406a5e31f96a4879e2adc6dcdca0fb9d932070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.17-alpine3.17` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine3.17` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine3.17` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-alpine3.17` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.17-bullseye`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.17-bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.17-bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:4329a441c8103b0542351e1ae387f43b06d99d03a78b6d680828fda55ed7a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine3.17`

```console
$ docker pull memcached@sha256:782343532db9f550c030b4c87406a5e31f96a4879e2adc6dcdca0fb9d932070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine3.17` - linux; amd64

```console
$ docker pull memcached@sha256:b50c3fe44c91c5528112e4da9c0bad85ff5826d9b65512b6211920c91371e976
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2abb6b3e7caf15e9f27c6b8f9dbfc038d2c039f541e372e81fff670d976db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:35:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:35:24 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:35:24 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:38:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:38:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:38:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:38:07 GMT
USER memcache
# Mon, 09 Jan 2023 18:38:07 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:38:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc2b20ccc66e6fe145ebab6553a6df865329350c2e07bc9b6c1696776c5c490`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48605e8c4ba284754dff3dd72f3ace695b35df6342d5fec283c7897f4832c4ba`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 108.7 KB (108722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d196d0613c7af538a87c9d4a7cf509abab9097effb6cb908344e7d9caedf8`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 951.4 KB (951442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cd6baa8fe1568851d5c5b23759fa5a1c64688cc4a07c5aa6cca80871c06ac5`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3fe8ba83294a99206c2a4ae53f31e4050763659d52e29d59c497946b1f1c4`  
		Last Modified: Mon, 09 Jan 2023 18:38:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:747440838b016f791c633e4fdeaf5c37f38456e7d4b0d17a2cff9ef30f8ce55c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9bb5dc17a7e102e8526b477fed9f9675cd5f136ab316764ad8f2f0de9f82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:10:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:10:02 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:10:02 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:12:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:12:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:12:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:12:59 GMT
USER memcache
# Mon, 09 Jan 2023 18:12:59 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:12:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0b416b5379acf6ddb6d09e420734c756c5bbcec873596331e737836e81d0d`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0b8b0e39444dac753bcfc5943b8483cf6f876552ec0dbe454c3837ae51645`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 120.4 KB (120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5152d3008954b3f64453d31a9bf2eaa2acf9fabfe3f0cafaa0ee9c2f8c73025`  
		Last Modified: Mon, 09 Jan 2023 18:13:30 GMT  
		Size: 941.9 KB (941876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ea796fa3e74fafff8a6904397b55db4d97a6199bacf725b5dce8b4569f344`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c2f983dd7c1c31a752a5e11128f6e55b8187ef9e5d2f4a545eebc2b619e10`  
		Last Modified: Mon, 09 Jan 2023 18:13:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.17` - linux; 386

```console
$ docker pull memcached@sha256:69e1546390b57b7272c882b60280fb6844a1bb2bd964a835626b41834168a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbefc81180d4afac6b486afbb629639bdb7e05c865eab58c927b9eaf4a872cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:39:30 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 17:39:32 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 17:39:33 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 17:39:34 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 17:42:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 17:42:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:42:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 17:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:30 GMT
USER memcache
# Mon, 09 Jan 2023 17:42:31 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 17:42:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6438a68dd467fe1f13efe6e68b3ab5e398a9fdea1f87bcd36bc46f471305cd`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0943d1904363609117a4b95d94a10292c19f098e318eeb44aef051d46eaa3a54`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 120.4 KB (120392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774350129f501c4c00c5076dc8f753239f4f6fc760cc79da2909d7c15708e01b`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 965.4 KB (965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115497a9de45cd9e47cf1116ca4f0db213323e5caf020fe170a127a36aea16d`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0508ec4e36106b62990ece4670db1df2f46be371d91d7fd44eae19aab854`  
		Last Modified: Mon, 09 Jan 2023 17:43:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.17` - linux; ppc64le

```console
$ docker pull memcached@sha256:679d0aa82cdf58994a74afc039b6d92345c85fe06f852427ff11804575edc014
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98905101c4893e3fe0318f910d856dcea6ced00957933a49d77ee55c33c4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 21:02:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 01 Dec 2022 21:02:25 GMT
RUN apk add --no-cache libsasl
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 01 Dec 2022 21:02:26 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 01 Dec 2022 21:05:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 01 Dec 2022 21:05:38 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 01 Dec 2022 21:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 01 Dec 2022 21:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 21:05:40 GMT
USER memcache
# Thu, 01 Dec 2022 21:05:41 GMT
EXPOSE 11211
# Thu, 01 Dec 2022 21:05:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76353b0c8a5ad3d0c634400cf6d8106546e19ceff0272975c07ec21754a150`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ab872475a132ef994162a3a873f6db068691a8f8514f18575a5893e7acab7`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 125.3 KB (125326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3fe32d8319179c2922e486297b2fde578c213de71a92854b9d768b0303c8eb`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 980.0 KB (980038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703403fc4fc5417fa67548715326c22c285872cee82e42c674c19057e5acc3a0`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d0912f292fa1321a1b34083840e71b1722e805744796e6857e65e42bcd0f9`  
		Last Modified: Thu, 01 Dec 2022 21:06:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.17` - linux; s390x

```console
$ docker pull memcached@sha256:fc2cbb4600450466b73c095412d7b913c94f4e41bed2a3b341bbb17679ff026a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298e7526756440f584eed700f705bff5bcf1efcff83a3f261caba552e2858b59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:00:09 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 09 Jan 2023 18:00:11 GMT
RUN apk add --no-cache libsasl
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Mon, 09 Jan 2023 18:00:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Mon, 09 Jan 2023 18:04:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 09 Jan 2023 18:04:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:04:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 09 Jan 2023 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:04:22 GMT
USER memcache
# Mon, 09 Jan 2023 18:04:22 GMT
EXPOSE 11211
# Mon, 09 Jan 2023 18:04:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6ada7778c4d9548233088fb90685f273d5682349521900a35145061c82a6c`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475a389065ee916d9aae39b3539ef02dca178def2856c9f4b97f070761d59d9`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 112.9 KB (112866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104394880e79531276221234a9b29d200b1b3e9986c865983cd7dfcc011327bd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 944.6 KB (944649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72357f410775788f183be1a3dfdec439aff7601c54ca56079e13c91fda758e19`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1116de74f31ab441c5839ae587b4256dd318783467221205bef7803e127efd`  
		Last Modified: Mon, 09 Jan 2023 18:05:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:bullseye`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:71855316b3aeab3b34e715b37b1e1f132b1ff941e8dee105a10db31ee8652b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:9e581dde543f22d9efd661eb043b07adb561af5b048ce9776e89a0595aa8087c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32986721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5509350da5820ef2053afc32c3ca7e19d0fb6c08ed1d49d6a78cfb48955edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:35:09 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:35:12 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:37:53 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:37:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:37:54 GMT
USER memcache
# Wed, 21 Dec 2022 03:37:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:37:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ca57ad057aa05a889430483bed4778d529f6a0e3a9b933371053ded4d8051`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ecced4732848e3a0cfb26c4de09ca4975c190fa3b69f5c2e7cab410464a84b`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5fcaa5e390f76618bc40ec8d148f9765d37a485cba4519fdf0e2912a21dd`  
		Last Modified: Wed, 21 Dec 2022 03:38:20 GMT  
		Size: 1.3 MB (1256280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8a9586ad0e617ef0566484dd78de6a89c01d1df3df050a482a1fad6ffd1b8`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c42cda38190ef2bac71f086cfa2b5e84fa337d93780a7cacd31f78f1a36f0`  
		Last Modified: Wed, 21 Dec 2022 03:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:a59f098f919952f02a5a39936d824b17ebfa3856302a65990a7f564e8e907eaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30447826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99301d3f21cdbd1841847c1fe3667ebffb79cd8978f6b8508d09df6b2974a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:07:25 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:07:31 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:10:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:10:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:10:55 GMT
USER memcache
# Wed, 21 Dec 2022 03:10:55 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:10:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749d0c8b208ed026aee090dedb832bc0129ce185043674af96d2a71e9af7160d`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c01280de0dd08bfc296ee59dafe92b12fef27aa65af570534e15ea82d5117`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 316.6 KB (316647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64208aa0ee3a0792b5d2c65dc9b82a0abd0170b154e010bab4da49fcb039de32`  
		Last Modified: Wed, 21 Dec 2022 03:11:30 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c3ce5418c765f0ea86cf53988c2384518deab2210a52181ec73227dbc31a6`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ddbe645796e9323f29aa0533eef1d53f4b4f779a58688f6def6c3aa26bf9f`  
		Last Modified: Wed, 21 Dec 2022 03:11:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:0da60459b3556ec9e226bb724f0a49ec7602fae553b8bb944ce52b3f5eab66cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da47275d086ec0dd16f5ef05b543e2bb8153628fa76654ec1fa45e6569773e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:06:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 19:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 19:06:50 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 19:09:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 19:09:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:09:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 19:09:56 GMT
USER memcache
# Wed, 21 Dec 2022 19:09:57 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 19:09:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205efc4c86629fab9eec38ed60804e71d45192dbe0793c841876f7a4fe9e1df3`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495647c9740b4b568a6c890cddc811f3f1a0a1439bab2e01319c660ecdd1a93`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09211963a4d282f9104c2ec3ceab47a1e902b54091c5b8434eb6f838b4ea1a`  
		Last Modified: Wed, 21 Dec 2022 19:20:43 GMT  
		Size: 1.2 MB (1199335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0304cb3027014e8d37176ee1f22faa617139b1965660f8b4f9c8855b7b582d2`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dafbc7744615b25205dd7f87b31168a5506f16a95313346f332e16cc57c44b`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:01d5e0bbfc5708780928b71552da51a2fb217fa03a8194224000e22ea5018586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31633148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e869b4576f1412a068bf1bd1291d3b8d69151edcf8f91e9e4e447fcc88ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:49:20 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 03:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 03:49:22 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 03:52:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 03:52:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 03:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 03:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 03:52:07 GMT
USER memcache
# Wed, 21 Dec 2022 03:52:08 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 03:52:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54490bc8eb00df36c66347115ca29e0c90e6de38f317fd81a817bc7828e9071a`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815e30e2549ae2adc1b95f572499dd450ef629e6abebb26525f8f121c09df1e4`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 325.9 KB (325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898957eaa497c34fab095d15441ba422dfe00cbe7a4bffeef2888a846c7b5501`  
		Last Modified: Wed, 21 Dec 2022 03:52:31 GMT  
		Size: 1.3 MB (1257003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b45919ee1b5a9aa723727a84baa08f2cdb7f4d98e40321cf1f2e498adbead`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586f2c269b5f8974bfdeacb2eb56b01c17ee1c1bce9787989737aa6e5ee40ba`  
		Last Modified: Wed, 21 Dec 2022 03:52:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:5fe0ccdf057fd5e9b59b99cc938a613b4ad2e1f4acdcb662ec5a5ed960fe2a09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33764777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ba0798e33c7fd53645be21cbb8c18586d3762e2e7e2c93c84f379466ffc04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:52 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:22:58 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:25:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:25:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:25:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:25:48 GMT
USER memcache
# Wed, 21 Dec 2022 02:25:49 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:25:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f37d24fdfbb0b6691dbe09375fdb807ca7cc672261c72556d25c8e48be2139`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 4.8 KB (4776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5c25da45aa7d932f6d93a6a52c22920577c573de2ac7a13a66321f94a96b2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 130.1 KB (130134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cab7bc9f15dc4fc7fe259c49b85b2f7b8d0cd1776201b15e72869e3325740a6`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 1.3 MB (1253714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b40dcdc2f285d61893ddfb34b4ad619d3c22ad01b805ba2b1da273114098eb2`  
		Last Modified: Wed, 21 Dec 2022 02:26:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f14044a30fdf946f35b47864b3a7d81610b498b01806ecb4173253eacb5631`  
		Last Modified: Wed, 21 Dec 2022 02:26:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:ae796e4bc6ea0fea6a739ac783a61928a7f52dbfff89207308228d74e04548a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30994244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb82f4b7afbc38572ba5416d75ac758e8c129a32d67b1d4b2b57487c68fa5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:33:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 23:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:33:51 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 23:33:53 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 23:40:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 23:40:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 23:41:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 23:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 23:41:08 GMT
USER memcache
# Wed, 21 Dec 2022 23:41:10 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 23:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35361ff90c50519084dc562b4b4e6e5a55b502266e2cb9dcbf46414a5d1da9`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 4.9 KB (4862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8782ddb91580fded24148cd61fa123f390c29d92cf4f7a041e87fb1d83355b`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 117.2 KB (117188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733172bcda62230b08263291076570372a1a16740e6df85d162cf8b633c17a0`  
		Last Modified: Wed, 21 Dec 2022 23:41:38 GMT  
		Size: 1.3 MB (1251892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf328a9bf45cd9fb8e9b8e62c1f66788ee12e2e00641959f154671cd4362b2c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f71cf5218e1fc55e01b7698e3512ef692389b4dd614c40e44e18f0417275c`  
		Last Modified: Wed, 21 Dec 2022 23:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:9cf9a7148ad1690490acfcc7c31b8c91fdf9139da9dd8e74f27b6cc1cd9150e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2cf7a2cb90f3262ffadb5a58e39d0a56652712a2996951884b0ad9408fccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:48:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:06 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:52:02 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:52:03 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:52:05 GMT
USER memcache
# Wed, 21 Dec 2022 02:52:05 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:52:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d5809c8547e31b3fa843095112a6c425ea28c420c27192076b4056a3733c83`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24857f0696214493a29f31d91aa51a6b6324047d4c8c09e758a022684640707`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 357.0 KB (356958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a44f07ae87ca332a1db77dff568f5c666b8284f8d085ab8c755ddabd350ed`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 1.3 MB (1324145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e65292400a1f2b01f8b6db40dc6c1c012274cd7ac81a6d70cbc55f9bfe66d`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de04456dd5d7588beec731787faa2aa35556599c1318d48409bbe95b71fa30`  
		Last Modified: Wed, 21 Dec 2022 02:53:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:827223506338600be1976f4d0ddd96006b7aa32f6944bf841b871b2a2e6cd124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31201160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f31bde7731b2a09ce82a1555836180fd6396c5a543b2dd7e3bee9d19915dbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:49:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 21 Dec 2022 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:49:50 GMT
ENV MEMCACHED_VERSION=1.6.17
# Wed, 21 Dec 2022 02:49:51 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Wed, 21 Dec 2022 02:54:49 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 21 Dec 2022 02:54:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:54:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:54:53 GMT
USER memcache
# Wed, 21 Dec 2022 02:54:54 GMT
EXPOSE 11211
# Wed, 21 Dec 2022 02:54:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197709195a8a95ab784485ea5d20b66952b9d32f56dd741587b0893c3d94450`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f1ccb4b0c72dc320139f7331b244dc5ae8c0377a25fc46511239fe7cf2860c`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 324.2 KB (324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee8c3ccef672c3da5f9086d921e44786e39f0c1eff0693e7988d5acc39f0bc`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 1.2 MB (1241737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4393bd67eb7c689ff7194d69aa8fc7ec65005d127b77e2f14888f46e642048e3`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695aae4fc1df2a4b9d5168445a3bc814ac1bea929ab42756fb960c7fb87d125`  
		Last Modified: Wed, 21 Dec 2022 02:55:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
