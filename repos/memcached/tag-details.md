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
-	[`memcached:1.6.23`](#memcached1623)
-	[`memcached:1.6.23-alpine`](#memcached1623-alpine)
-	[`memcached:1.6.23-alpine3.19`](#memcached1623-alpine319)
-	[`memcached:1.6.23-bookworm`](#memcached1623-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:94014d930e4ce7ae500de4edc6726f71f14d80ad94762a000b65214bacd5e754
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
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
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
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:a21164326203060f065efe61a72fb55df457dc1aa9b662533dae967182897180
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
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
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
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:41d19476c100c4b22a07c635e68d4e94e332eadd3afbd8f6bc61cd754d9b5d06
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
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:12146749990ef0b47274176ef1c67355add55d855a26ad1a6c1e0824d38856fd
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
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:94014d930e4ce7ae500de4edc6726f71f14d80ad94762a000b65214bacd5e754
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
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
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
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:a21164326203060f065efe61a72fb55df457dc1aa9b662533dae967182897180
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
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
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
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:41d19476c100c4b22a07c635e68d4e94e332eadd3afbd8f6bc61cd754d9b5d06
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
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:12146749990ef0b47274176ef1c67355add55d855a26ad1a6c1e0824d38856fd
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
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23`

```console
$ docker pull memcached@sha256:12146749990ef0b47274176ef1c67355add55d855a26ad1a6c1e0824d38856fd
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

### `memcached:1.6.23` - linux; amd64

```console
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23-alpine`

```console
$ docker pull memcached@sha256:41d19476c100c4b22a07c635e68d4e94e332eadd3afbd8f6bc61cd754d9b5d06
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

### `memcached:1.6.23-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23-alpine3.19`

```console
$ docker pull memcached@sha256:41d19476c100c4b22a07c635e68d4e94e332eadd3afbd8f6bc61cd754d9b5d06
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

### `memcached:1.6.23-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23-bookworm`

```console
$ docker pull memcached@sha256:12146749990ef0b47274176ef1c67355add55d855a26ad1a6c1e0824d38856fd
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

### `memcached:1.6.23-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:a21164326203060f065efe61a72fb55df457dc1aa9b662533dae967182897180
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
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
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
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:41d19476c100c4b22a07c635e68d4e94e332eadd3afbd8f6bc61cd754d9b5d06
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
$ docker pull memcached@sha256:56b3526ad7eba067730ca64ab7a9062327160c9ff6dd9bc6d84fe0cd36b9005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4023415fac5142ff389e46030788e399f2123c8faf27e3a98b48cde1e6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dae630dc039dec3a0adeb37aeefd93b0ecd62e8fb8a2a5c7a66cf6cdb823c`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b00e79d37f41df7f21a0a02805ad2113587ee208f882c4b175bbdeaf78c7e`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ae6bf9726297775412e5ea64fd218ebec00e9aded2126f58c7d445fdc6143`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 948.7 KB (948697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930b8ad8152fa665650e6ad9a8e4e30c01865a5bfb217b8abdc2a4eab5d9cbc`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea93284d0d5680d9ccffd5aaa547f32949cd01f9e770fbef01a07aa9fa88b57`  
		Last Modified: Sat, 27 Jan 2024 00:56:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7f84be0d4b8c824dc33800c8180abda9d9895b6cc931a9ddd4769de1d2bd8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd68fa64ae4a64e252a2fc3de47be2292f66a1000d9a74ec1a4df71e140d6935`

```dockerfile
```

-	Layers:
	-	`sha256:ff79710a1992811163cfa3714e2488e96fb0b1c1adcd56600fcfa6445adc3758`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 78.6 KB (78609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653be2b79d371fc961d5607d7bd8e3ee0fbdcd9dc6aa564db6d3a5f4ed6a9a91`  
		Last Modified: Sat, 27 Jan 2024 00:56:00 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bf184a14585ef27c8248c86fc4b7720d470388144f78d47be37fe579906fae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc48d7b6dc8c49550af55cbbb65468e1e8b2d39693894702e454e7cf128f5f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab01ce18cbc10e51077995d9cd380b544d614e9e9cdf6632f27f6c9203e2f3d`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d4c0cb74be17f61da6b8669b0871de75d5876c7f0c8225c74292820b35fbc`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 120.9 KB (120893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf36ac46bc2e682c926d155e3465ab13ec470212fee06353705e08d4634a324`  
		Last Modified: Sat, 27 Jan 2024 20:30:41 GMT  
		Size: 949.2 KB (949177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f26735ad30d32941cbac9dd4da57fe39beea671781802ac901c6b4063a4e2`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b8fa75d34bf5366ecd0ba0b64ef72e972303a0e215a35bbff039d3b1e3022`  
		Last Modified: Sat, 27 Jan 2024 20:30:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4cff55d1cac76141a1936213b67539c2521165a933fcfd9f97e4a75da50ac4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91e61776c3bf0ce3f1e90487f03e58d2cc672fff80ffebc6019283bdb8c620`

```dockerfile
```

-	Layers:
	-	`sha256:42da215937ac30826e454e9fbb0ba3884cf66095edd526e0de13ec3fed1cb70b`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 78.6 KB (78628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952c1690be0c94da6dffc58056acf3aaeee376435297f0aeb5f22de2d5133708`  
		Last Modified: Sat, 27 Jan 2024 20:30:40 GMT  
		Size: 19.3 KB (19318 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7ba8dec2cd0118a1fadd8bbe004b3f07212a361be8d23809ecff8efa95848534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6806686fbcdc09590edf1c6b1e99be11feed8c739af04b1ea8f4b976529f3b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26923ec46171077bf43a623b86b87fd0412d452a45e916a77e380921a11fe162`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cea98c7b5cef10d6a1962a63a4ae4633c8a353c9b9293e81bdd9aea56784d7`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18dee2b5ac6182f64e4cd491b58abb5d796a9301d0d34cdc66292127c7e8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 939.5 KB (939549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7661747688fe0b3c713c7a13900025789fea645c3aea30f71f68304856eb8`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e1bb4930b8105acc77b24827d688be7ca4ea4188f5e0aed208ca36057afbfb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9e95530611ba3545a639995107e8636aed3a9193e8bb4bd62592d415a623bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d2a061c4a4669524c926da30186686d6c4f5b9e114ce48d624653931090fc`

```dockerfile
```

-	Layers:
	-	`sha256:9730e3c3f8e8ade3b4e688745332c337610a9907d55ed665b7a37ec9aff25173`  
		Last Modified: Sat, 27 Jan 2024 01:56:49 GMT  
		Size: 78.6 KB (78564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e83c97c6c8219a3d4ec3c6c04cf158c49855a27216528a9be808da21238bb`  
		Last Modified: Sat, 27 Jan 2024 01:56:50 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e0b61ea6d2b9e211f9eb5fa7112a10e52af4fa8343a81c28a4ab1d367e4595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144a53c38c6a648731fbbe08c815d0ec64de3b34bff205362b638e988996165d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4e9e66af1ff82abfaf0f07be03d1018a109a88d020296b2b8a731b4107e5b`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54757f09b59fcb1db18af56e26ed6f6e0d97c5aaba3f884897718b0bf5f24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 123.4 KB (123393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ca251b758a859f32b5514c12f2dc7f41d8064397fb8aad31de5b4624439f1`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 985.2 KB (985228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd874380e55fd3d9cdc3d21b4e24ad19619ce788affda34d468a79a4c7e1dc24`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839df7e671c4ee89ba2e7dac90852e1c94b82c961585e214790e11945ebb600`  
		Last Modified: Sat, 27 Jan 2024 09:50:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:600ba3510db5ccdf8c75633ffa679e57a341e5588f6bdd8ea25ebad8c9ef6c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a43399757d6716f61a97bd6679bdd2e0407319001eabe940840c1bd8ae4ff6d`

```dockerfile
```

-	Layers:
	-	`sha256:89679c50e87992a02ede8e879ab439858a379ad6c02ebe2b33246cc610fc8735`  
		Last Modified: Sat, 27 Jan 2024 09:50:17 GMT  
		Size: 77.0 KB (77031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2a8a4d5df2efd18244c9dda7757bce62a4c39fe336f4cf8aa5f448d2f816a`  
		Last Modified: Sat, 27 Jan 2024 09:50:16 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:1aa61f604e45e34b0925d20aee59b7f622cafe1751fe7ddcc2c73ff222e64b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26862952b39d9710ef9e3cf9c4e05b26c134a56637eb287c0cc4c465dd0951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487336cb551b2d4deda866426c3f529b779d41105462298c373db34bab2451c`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4736d820946f29ca7b86bc0a7f9ceebe05b72191c3f6e3fbd70d08751fbd967`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 113.1 KB (113135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f04768714e1153eb370aba02f0d4de13b83f952d99e8b98cce61fffbcb0dd`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 969.7 KB (969698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7788b8b0f6eb81d8f54a773ffc88d88bc5fa371e6100d7c8dd77fa7fa311ff`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8f3e93cc28da9034c74ece623c8ca9d8a5b8b273c3cf6abd66050dc95e413`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b4d4eb96dd2aa5e4c6997dd27021987f6ec3f5c8c823149a70e24e5b7ea4266f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96e99d1c01214be536dac6d27975061d5716db90c39601e6b858b83c21d742`

```dockerfile
```

-	Layers:
	-	`sha256:ae20e189212cbc91208e146ffbe588060d27d24a33712c2b224b6b180033957f`  
		Last Modified: Sun, 28 Jan 2024 09:26:58 GMT  
		Size: 77.0 KB (76973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954eec1c803e884f942a36700061dcae5fa9156bbaab5a575507fad1bdc02b`  
		Last Modified: Sun, 28 Jan 2024 09:26:57 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:12146749990ef0b47274176ef1c67355add55d855a26ad1a6c1e0824d38856fd
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
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:94014d930e4ce7ae500de4edc6726f71f14d80ad94762a000b65214bacd5e754
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
$ docker pull memcached@sha256:8318622cfc6a9dd7f1ccfca74ebca3b82918067974f36c47ddd470a3d4e5c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38787917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002d0c8b77b7e964b7140e212c314e181f2dbe5d3283921714f0e27cdf22c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50513b7ca354d8cbd37b70475dbad24d83c224b287f6a51d0a08765caf656`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bad658326369c7c222afd3dfe577ddde65894c812a79b3899ac3a7043b1222`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb85b88515620b5e746444549cbcf4e78a5fa958c9ec191ffa21c8f2b9d606`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 7.2 MB (7173818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e83ae2e004600cf67678d7afc87c0bda4c8f98946a25d9585426c5b4e33f2c`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f65b5ce1c0a837e3cfe555f5bdaf2ee65b3d0adeae3abd1332492545722fb`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed2f71f4972eb3c78d858772563095deaf8f772edb559ce583cb8047e8f056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ab7ba1962ef98e4047104357a8e1b28b48f73a31a730972ce2807c1ea9bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c41206fa5dfae4cec6d95eb96413738185c0bdedd7ad8bb7be26e0268a4f7e7b`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 3.1 MB (3056908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8fdca051d26b2aa41e4c148fe3f1c878d68290c575e68d3f343fbde3a9e0343`  
		Last Modified: Tue, 13 Feb 2024 01:56:38 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c09f5e2eab5a5350b6f5558d9f4a26f556d74f46eb62c2b7e4e3d02ea956a634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb5733a441822e7bfe0a68e5a667e78b0cbe2ff291896039b46fa39e3a92ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c372865be9a6ad8d551fee81350376c9cc18181bcdff40b1db82f4e65dfff2`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 5.8 MB (5835451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aaafacc810fe35bee178a34ca4618f057878f2f2f7f74eaf065757d85fae6`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a43dd78f5c7c9d33634fc1d864d93254dfaf8f16ca552789486025641486ec`  
		Last Modified: Tue, 13 Feb 2024 18:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e76164719829a3e2b3f9847dcae81beb57827b638cb19cb26df50a7a5fabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b127ef08a7e9b9ed7a18e1b245513fc479ed2cbeaaddfdad2b13072a322a82`

```dockerfile
```

-	Layers:
	-	`sha256:5970a8c1db91d8722c57b65800d0c4d6944eeff5adb08ec99978336158e03f49`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 3.0 MB (3031640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce39ab61b403801df7a1fa3125bc43cceeb714a42988d35605751a6d21153c8f`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 21.1 KB (21091 bytes)  
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
$ docker pull memcached@sha256:38b3b5741fcd7e43872c8c0e2124022dd9da3fd39e52098c77a0389bd24a0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dabe9afeaf94f4a2da5e3553e96c0a2a5f17a21850252ddfe3f9e6102499f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b3d73ddcc820510d6240c578911419e080bab6fcefb37b447e9d74a3a9efa`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 6.2 MB (6182268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d11f9410d9d361905bab185c8dd577f7201e75ca189dca4e29b7864bf09ecd`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9274826bc50315ee5af52a06b8e14295bce821e16265b6cea4f524fcb6fa2b4a`  
		Last Modified: Wed, 14 Feb 2024 00:46:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f37755c1cc54669e1240ed2fd51cc233fbac22cc563784ce4ad38eeff03164e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe49adc1571c6ec09005a052566a2fa2c3db3d4a637f017550bbaa83677d3fe`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a25bc1e5aa7d52a9d24fe4199c0efc394cbf0f3f351e327ea9867494391e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 3.0 MB (3032099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2963e1444aaf31f424ad82e56fa709b4ec31f52279859c0a5aa9d5236be21e`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:341b9df9ab365703da97486546bc4678e8041d055f7acbd02ecb9b4f52380e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ebab3f96d3423a155e1f3d28f85abc1a81e1dc30a7b2275c6c9eb53cfc1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896cb0d95afbc658063942e5a9f9ff954354827fd74681ae64b7df0363ec25fd`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65440acc2edb17ba20c8c2b3da71770921e726e892e898dae334ba17cdd873`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 2.5 MB (2492649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aeda5aa13728cbe709407edf36fbb695d0e1dc4ce36bae4c286ea28ed3ebb7`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 6.6 MB (6635197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3c39419649908d9c6b8be3bbd95ba8b388a1fa39592cc6109da0578c50b12`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ea9e0e750c13e4b124bec532f41c9608de1383352dc6f3293f3dde78102`  
		Last Modified: Tue, 13 Feb 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4c73b2697e26f7f9dbc63d131c3eeff4ff80afcebc0822c1f72965b92787bb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbd8d207719b6ca50075b571ac604f12700734b3e87d3893af17d9703d6f9d`

```dockerfile
```

-	Layers:
	-	`sha256:5ecff55ef50addef8a3c65c679ada13b270347119d29f05bfcb68aad4a752502`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 3.1 MB (3051211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf1c33de5b630544c86a7dc863f03924bbc7c9c33d98f2da475ceed39fd17b3`  
		Last Modified: Tue, 13 Feb 2024 01:56:44 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:55c83eee2ba582f1d921f2eb68a5109bd8449487715c7f4ef88fb5c0579e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37588835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8557f165694b488ea17a0f4f30f756cc15def605f24d7505ced61b1cec433`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ebe543071daf608f55a76b163505b7117bb855b3e4dec964e04241c25b8ee`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7fbfbc45c1c5aaf22ec2781dd149d2a47da448b91426fdb848fdedcc0043d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 1.9 MB (1937503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51bb9ea6564b5e824ff3ebf2b49e82acedefe3bf7456e7f602be73e6f0d0e`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 6.5 MB (6507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159ab9da3b86752e9e4628934b7ed18e4a76cc874731105934ff29e3391bfe`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90c49c697b6c359f334f097072327a2a2ac7a2d17961ecd6cc4d25792fab2d`  
		Last Modified: Thu, 01 Feb 2024 20:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:401e514425035d39398e1306385e86aef43e265ca16cd52b8b1d411a401ed4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5f8f3b0aa7733ced58f7590ac61a0e27e8340dab6783fd247219d2e096c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c276424e57f3733b073e6168a756d230675008a970a945cabad35cfb19d977db`  
		Last Modified: Thu, 01 Feb 2024 20:22:11 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:de12d05c58eee8e76b3c9ae85f3618b1278e5fec7d32907da8d6eb0c4e34f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d795771bad9ea1ab47ff373c0c680378b2f5e203c66979aeca5ff3f7c8280b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d281607549e24e6e33fbb28c7dacb275e8a70bafc48fd3400fbbf7071bb3406`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 7.2 MB (7187022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506870495a80f147f903d1dd3ba776d56591cab330288d85c98123c90dd5ff`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb678c195d3f0bd7780002b58efaa37d67ac5f70111cdc348f99067984171d`  
		Last Modified: Tue, 13 Feb 2024 22:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4a494ff4a4f21ca42c4a8100d02a3293de27b73fcee4465eb05112f7b8eb2bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0696700f82e6f55aae3ac72019f6beea1c1cc814040f0b124142023bd1f26e`

```dockerfile
```

-	Layers:
	-	`sha256:8389bf9f7f747207d5a88095f1f2e143741df1424f0124935ffee2dba0845229`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 3.0 MB (3045494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e051d504e29e43bb84e5ff27357d962b0ac91241e865871ec0b78d609038631`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 21.0 KB (21016 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:a03fcc98c278ed7c8bc5faa714b4e245e827ae2151a982778e990f672d0d23fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea24f172fd0f0787f899927cde354580d44dcc35b73a856512cc886215dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124a918502fe434f438e3c14fd33bee061523804f1284062bdb4d155628f0c4`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885dcb2db89e2f0b44186c54bc242636683124727043a129c5a64cb0d32e94`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 2.2 MB (2152509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d519f026dcd1303d7af015b3c0ff5ea0554160f3f150e9b381a4d8f831e56`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 6.1 MB (6080113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8da939feb41cbb22259dc2ccdf450ed20342867820d584b574d1f7d1748ec`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce670d68ccad027814d20fa0f751502188055ca04561e1c08687e803901754`  
		Last Modified: Tue, 06 Feb 2024 11:59:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:260fcc9ffca88d5ca1a6fea223816c3388cdd11222241cacefc04336915582ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115b2e5c62d2ef242824f609c442689c7937f592e796fc9f8c09d80ef9c9366`

```dockerfile
```

-	Layers:
	-	`sha256:cf80b56a3e03ea3d08d9111c05e80b51224a1cea82b99d4b9d7a4c6511a2c55c`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d43917d7ef6b12be2e240012f95de8a4080fd9e4776c6f29cfbd475b7706bd`  
		Last Modified: Tue, 06 Feb 2024 11:59:33 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json
