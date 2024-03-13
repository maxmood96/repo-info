<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.19`](#memcached1-alpine319)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.19`](#memcached16-alpine319)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.24`](#memcached1624)
-	[`memcached:1.6.24-alpine`](#memcached1624-alpine)
-	[`memcached:1.6.24-alpine3.19`](#memcached1624-alpine319)
-	[`memcached:1.6.24-bookworm`](#memcached1624-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:ee04f5b1aeb202acfec76d75d44e6fd2c6959105fc12f042f257ba5775a3066e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:5e2c26a27f53501add6d8eb6b1cea7897e32a3bf78889bf007929a615a8cc09e
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:a06c895acf0a327fce4484739fb1492c5e574baea878a0a31d8879d2476a45d4
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

### `memcached:1-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:9232f48174d2e94252ef10af60ed5482a1fd81293acd6079b7a221c856e5b24c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:ee04f5b1aeb202acfec76d75d44e6fd2c6959105fc12f042f257ba5775a3066e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:5e2c26a27f53501add6d8eb6b1cea7897e32a3bf78889bf007929a615a8cc09e
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

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:a06c895acf0a327fce4484739fb1492c5e574baea878a0a31d8879d2476a45d4
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

### `memcached:1.6-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:9232f48174d2e94252ef10af60ed5482a1fd81293acd6079b7a221c856e5b24c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.24`

```console
$ docker pull memcached@sha256:9232f48174d2e94252ef10af60ed5482a1fd81293acd6079b7a221c856e5b24c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.24` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.24-alpine`

```console
$ docker pull memcached@sha256:a06c895acf0a327fce4484739fb1492c5e574baea878a0a31d8879d2476a45d4
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

### `memcached:1.6.24-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.24-alpine3.19`

```console
$ docker pull memcached@sha256:a06c895acf0a327fce4484739fb1492c5e574baea878a0a31d8879d2476a45d4
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

### `memcached:1.6.24-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.24-bookworm`

```console
$ docker pull memcached@sha256:9232f48174d2e94252ef10af60ed5482a1fd81293acd6079b7a221c856e5b24c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.24-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.24-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.24-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:5e2c26a27f53501add6d8eb6b1cea7897e32a3bf78889bf007929a615a8cc09e
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
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
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
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:a06c895acf0a327fce4484739fb1492c5e574baea878a0a31d8879d2476a45d4
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

### `memcached:alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:a97fa6599335ebbc785ac1c0f0debfbeed0ba43175ee6ef8b2f637500f4e6a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6020105d217333c87e615b6c07c26b0825058e142edd7829e5812d74750066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3b860c43b748844d7be2babb634c39061b30b79382481bb871a015f656afd7`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba004b05b65e2738c846f8a90108d3497619178c20fddd64dfa52b6d96367a`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df821c7ceaca4ba8b2353eb065bbfddfd27860f52eb23f357a5bf5b09294e3`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 948.8 KB (948813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d81e1dfd37f25b653ae74dc966d87d21bf9f5fd9b6e58c05a674e5fae68ee`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d198838d3ed6bf76c541b51d2007ec9fa1c894b0baa95552176317e8aada5981`  
		Last Modified: Wed, 28 Feb 2024 21:52:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cd849f38013707729877b7c40dd7c04e21bb0ebbcb3976daa962a157a392aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1113c7bed2458a983fb97a2c432924d6dbf37edbf00b1f9b2fd6ba32bf72784d`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfd93f99a142552efcba4aa8f94f39a772aa5f5f98078a5020415c87ffd3d4`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8685b54c31215020f930e7c103b901103d625381b0e5c734e87076fdc750033`  
		Last Modified: Wed, 28 Feb 2024 21:52:27 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a44ea0eae98f4b5ab3375c95f65c9101f818c8b02c6cd58b5da7a886843c6d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b49314251306d3e41ebebf23875590a1e23f1b6dfba6183101ce4fb95be73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebd5577c9ad940cfd6243cb2a9132c98afe06ad5fc3ec7a58016f6b9382f6ba`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842bc308b4b44fa092e7cb6e9c923a07ea37dab1e13de8c1609ea5bd4216699`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 120.9 KB (120896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f391a100c38e95fdb9a37f6e140474f04c3d5d42f6b444bf6792b9266be89`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 949.7 KB (949684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804636ae594de2db38069a31aee3e48341ee645fb5c6909a7223be7b0456182`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717be6425d1b691e2224e1e41f01527058d44662c7e20937edb16eb6ff06c6`  
		Last Modified: Wed, 28 Feb 2024 21:54:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:f8acc238a0feee70bf132d7cbc9ceb012d4c679cdc02e030966903abcc575b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e679953ed62f483fe9b85e93011b70409ab2c26b166e9012e7cbc942534fa`

```dockerfile
```

-	Layers:
	-	`sha256:51f3d55b8460653d7c6b33d35560d9476430d3f2557b89cc1e79b99cdc20bbf1`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ab102c26d722fbd7bca86ad1a5e41724e7de048fb676a5f4e6bfc7aa7b2dd`  
		Last Modified: Wed, 28 Feb 2024 21:54:23 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:5a4b1b3c200cb15a8948a34ffd040d3af2d802a5cb51af6c08f0e3ed1a0589fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ed3cd9d51cd78852daf895a3273ac5d32057edc03411fa6ac5974898423e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0a3b5501e741c16357b48ffb8f0df63111de0dc945ba768967dd092fd540`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92c884be5315e7ea73135b9380c457f52de9b512d0981cc9e2611a064e8749`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 109.3 KB (109325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ddff442a5fa306ffd6dfc5338a6bbe4ee5bb256b3f214b63eb68ced74fe75`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 939.9 KB (939910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd23e972ed0e79483d0646dc3b27fc170c2b6ed583baaa95c69cc94c6af9c6`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce4e4eabfb72d79f0e63fc3d621d17105b4410b8d74e7527119395e9f5475b`  
		Last Modified: Wed, 28 Feb 2024 21:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:edb93f9463534108cba9314a72f4dd4aa82965dd00bacc62e699522826ed2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b77b9b3b03b85249268cd7d7197047354fe74c43b2d2a6e37691413f32271a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e89f25a5df0782495f7f3e23601ef84a03ad520a22104424d35ee55f446da`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae5ab34c68502b8d679b7a87cebd2f09bd748e65156d5d211027a36be997263`  
		Last Modified: Wed, 28 Feb 2024 21:52:32 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:c02e3031e8c2cc2d9fe1ca22fe19cfeebadb6986a0c205bccc9a0008b8c9dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437bfc8c334c403275f5497df8ad6cebfafdd3eaebd3c42ae77252ff2cd7767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508fda8fc6d9989bd8fa04db2c05b2eab25a99aaa5288b67e7be208e42b25568`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bcb656a453bfabd16f2cdf5636de6e70f5728b71c0dd80612b58a95208e22`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 123.4 KB (123396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f373c2970def7bbf7d7b066a1c68c20a6b2a53b6a6c16b3604f2fc3ae1af88`  
		Last Modified: Wed, 28 Feb 2024 22:18:08 GMT  
		Size: 985.4 KB (985359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e56806da1447b82ec8015e12cf8eab38effacc19facc75e3ab8f6d55eb28e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0da37df703a4d0a988359145a21665445c7fa9ee378a27819d84f7b123b602`  
		Last Modified: Wed, 28 Feb 2024 22:18:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ba8662c07d795062927569f1c61e6f60e0d6fbea5dc14f0beb3985d2033a3ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f82834da87718d9d6448c1b872a6a84b8ff912388b2a88ec6d93066b43e0d`

```dockerfile
```

-	Layers:
	-	`sha256:e74b4b12d87844d92b8522db7e0a55c6ac2c90c0afa1c16f647d07788f6fb1a5`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b48d39eb1b87da3add64e637757bb82eb098b14e90783c10967edca2119c07e`  
		Last Modified: Wed, 28 Feb 2024 22:18:07 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:3cede7cd2f95274da80774fe3315740ae77c880eeaa73c5fd22852930490b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e42553a076c8725ebf3a20f0a46eacdc4dbcd684bd77c10855503c48e22e03a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab190f1456ddb39292c70dabf89f2be8973f139fe0927944514665db4bec36`  
		Last Modified: Wed, 28 Feb 2024 22:20:15 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e732258aaa9e99b6b4846f278f4f87bebea2c1e296b14578f2322e75b7196`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 113.1 KB (113131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2d7816f63b196947a0c722fcd8c6f8a4d2355a32009da35604f8d66accd7d`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 970.2 KB (970153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec314ed1d3f3f7892a832c4bbc5b463eb7ecf9c5a1e35d370650da008dccd056`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c55a39459689f480cc0af733c5a6e20d06ef7296f8a5e8b95926c57c01379f`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f54d9fbda178189ae34fe9f330ab798c6d79620372984266eeeee6427ab9635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79a37eaa421f9308c3fbea694b8ad18480c63cc2244007ebef3ef0d1df8baa`

```dockerfile
```

-	Layers:
	-	`sha256:01ff22fff6583c00712fe9898c3846ef318285cc13d2b7af25fb6b8f846f040b`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0df2b7583823c4dbbfb4b1de60e8c56b1dd28cb9feb87259545858303ad82a`  
		Last Modified: Wed, 28 Feb 2024 22:20:16 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:9232f48174d2e94252ef10af60ed5482a1fd81293acd6079b7a221c856e5b24c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:ee04f5b1aeb202acfec76d75d44e6fd2c6959105fc12f042f257ba5775a3066e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json
