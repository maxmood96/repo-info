<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.20`](#memcached1-alpine320)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.20`](#memcached16-alpine320)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.31`](#memcached1631)
-	[`memcached:1.6.31-alpine`](#memcached1631-alpine)
-	[`memcached:1.6.31-alpine3.20`](#memcached1631-alpine320)
-	[`memcached:1.6.31-bookworm`](#memcached1631-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:1.6-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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

### `memcached:1.6.31` - linux; amd64

```console
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31-alpine`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:1.6.31-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31-alpine3.20`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:1.6.31-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31-bookworm`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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

### `memcached:1.6.31-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:d5f0538e1d5d444baaa8f1c396ee3ccafe46623cae858ca5359ebae153603074
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

### `memcached:alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:d4ad31d3bd7795c67d2cd13ba4dd6cbe7e5fd98b6fdb2c65fe8899c1273863a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4a945310d72e622d9e296e562586f879bbb98d8b5d2253e09a265d8970218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58159664244b73cfd44f645af783aa97a0e142641257e705b340ab9105e564`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d92ba4ff123d554e1fa042ab5622665150c418f60f0b849e7e90fde9343346`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 108.6 KB (108588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834574eb3076c49fc741e2249afabaa5ec3fe475135fbc37d76c0a052d956c7`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 950.9 KB (950856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23cbd28dd8e2fe9af4ce27dc3f3e63209855cab221e94d2f1f5bc33dad4410`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf928933f40c4e7b4613a9fb48e8d8d4f2ca277499b1ef1c6ad3151137e472c5`  
		Last Modified: Sun, 13 Oct 2024 23:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c7adbe792afc3932ed6e1c9ddd143410ec018f508543c70630e092465025227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 KB (105354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5900a4bbeed094e615852ad1691322e7a0b6b16f22b49490e0b9775b8e42a467`

```dockerfile
```

-	Layers:
	-	`sha256:949c5c7d1c81aef825f8921852129960718c9e20989f159797101fae1d3a5686`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 85.9 KB (85898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903e83b6b844e7e301242b1d0a61b63cf556ea5a470589d87431eb8d7e444196`  
		Last Modified: Sun, 13 Oct 2024 23:58:58 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:9df0ee6dcb9dd42fe366335425791cbe42e722f6dd57b24706d058b1d38837d7
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

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:ebc1c85c752a89bd56b36d953f6f0759d64bb9c5f4dec0748b808ed6d51d206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047d324da0626b6ac887de92ca59f283b6ad9ed9039ed7c6a68fd939751e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0775f2ab59348a18e280341bc51187fa38ebbbc08b650cbafb1f89263da91`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2c89cb8157e9987d331800d61e43dff1e060ae729bd5e1b7f922d292f65c8`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.5 MB (2491339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a93d23277aa454146564ba40d242b824503d9cf135213fcf9f4f1ff01b98db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 1.3 MB (1259263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d19e499284f9fc28b78492cbc68e0145a0775adae8e3f8f43934e7397804b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26564d4f6b003f5652d54d26055c8019013e69f93eb028337be42c7487e02`  
		Last Modified: Thu, 17 Oct 2024 01:17:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:356d97a39f93624d31af2b2c6d5c9d8f8b766503d5d5ad7f8704ee99f0e72a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4f2608e74bbbad3a7ab66ae28feab6ab838982c5ff95968cc64aa138ba6752`

```dockerfile
```

-	Layers:
	-	`sha256:8f2569a523f4dcc02c012c16bbf745a932c9e10ec928db2d842be64b2c774f2b`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df34ac306975dcb7daa686f687f83ade67d413e47a74e6fb4fa9b15a91b66db`  
		Last Modified: Thu, 17 Oct 2024 01:17:12 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3b854b1fad95ab6ce7154c9166778ef8f2af4f627f269c1ea72678607a74c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f555b0f31c9f2dfaff14fbc48a65c621250c42120c4e8d55d21588b63ee736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933165797847338547e5f44f2fdd2d0912805b02c19d2de000c8ba14daf1b0d`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45979689175c16711a8c540652fa8f45240c4a46b2016ddb5ae1c3c437f4b51f`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.1 MB (2095622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5256e5d8a5cceed236033f5b47ebc5d3ca503ed71d9c457ee71f4dc21aa49c2`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 1.2 MB (1238219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e174d7badd0e416fd6a6e15680e6a9143c85970671c257692ea6a61e6ecb6`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3305fe1ac0abf9efbf62d20adc116eec31baf13d96f573e1ef739e56f4b0ce7`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f4ae44539792e0b2a5b244b0da97c87b8cec996bbffc0baf10a4466b8061e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4ab1cef680c6a66d7a74833aa5589486f4b17aee8769730b47b2e24762025`

```dockerfile
```

-	Layers:
	-	`sha256:2ac13f374eb29f6516ef3e44e297182618b506b17756e17557ca00f11985d7bd`  
		Last Modified: Thu, 17 Oct 2024 05:49:24 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2663c85f9d9ffd764a18fff8eca344a16bd2e84f736f94b9d4eca0cc71534c4b`  
		Last Modified: Thu, 17 Oct 2024 05:49:23 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6fc0b35e05b20d655fac22cafd4089ae62e2b6ce36e5cc4765ada4e4a5f509bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c4f79c32017ccc89271290c74ccbb1e73bf3677c8627a1f4d1dbc39e7172e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad03f1286870a8006f720920b2f6742e72977e578573f945527da47d562a98`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b37a40b5c0bb1161ad8389673db4e7626e904e43f988a59a26176f2794b4eb`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.4 MB (2354807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eca40974634fdfa1d6859ad37913724ee2fd47d66b25219ad7f0c515d7dd31`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 1.3 MB (1254708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e61ea9eb33ea8b104269ab1c7a98610185e84b135b05d1190878929116bed`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792dfd57e427ebb7a4cf24c8ad59014ef1ed600105a1377ea326428e37e9a8`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:36804c8742bb41bd58b3b1c89d4005fe1c00b289f07456c72280b3d0a1f7d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a4931d6244c3c7a9e38db37d7535acb74c72bcff0a2d50702c4a11736f9afb`

```dockerfile
```

-	Layers:
	-	`sha256:91d78a4eba84e2fb1a8ab1a6d4b1d2c192aaa151bc970a67e879b263af40dc3d`  
		Last Modified: Thu, 17 Oct 2024 13:22:21 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3444022cf5f4f61faedcfdaae061381558260ed3a9809dbbb683735b1a2f3697`  
		Last Modified: Thu, 17 Oct 2024 13:22:20 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:bf299b88a3f44ebbdbd88d44caad028c906c61618d3b0ec1f034e7f957a6e3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c34f5b68c3c2cbe20a439da379d656ead457b47bbcbd186535e25c75b9d80f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e042a201789ac498eb9740c9a408d31b718eec5018bba03d594d1aba4b2a2`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541cc871445f2280535f8396971b95828dafc21ffbb99d4f16a5dc5c65dac13a`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.5 MB (2499296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87aae2edbc1db09151416059b91c7d5bbbe18d1209d21db072e4e1024366a79`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 1.3 MB (1259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50b505e9b7463993298860d6040c0efff6c2f8f32dae99f095e922aad901c`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6bf59e05476d3cda1da00fccc8f8d0a3ddad0a3ed724c34961ed7f3d0a44d`  
		Last Modified: Thu, 17 Oct 2024 01:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bffd367aa8e2f16fb0b8bb6b6669a754c0a7ca6fff73f41a4eaa48f2ae361ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967642d32d13cb31fe97fb8ae0532c95440164ddab03e7905d760fd5855a331`

```dockerfile
```

-	Layers:
	-	`sha256:c8800a2940aaa1747c7af22d0cb357778a99feef0a164658399321cf41e15c56`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e0523a312592a28ccbeee3508c8d81250369b535fa923da168998973a9d61`  
		Last Modified: Thu, 17 Oct 2024 01:17:21 GMT  
		Size: 21.0 KB (21011 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:cd18b0e7ef6a9d092a53aae5a2dfe9db4847e1d865dad8a1c0f2474aa551d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46016681cdf97f6c4f58c8ffc720acf8b48fdc363065ae254b28a74f975a3000`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89af18ed6dad2d50595a887bd4e557d7dbeec54c9d7292891f173fb8248dd738`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4af78636d4d70d8872577c825a64d60618a042f7aa993255669ac916fee20`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.9 MB (1942693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a61fc0387e16cbaf4ad7d58581295c77126c045f4da729103ee15b35cd6fb`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 1.3 MB (1254474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7cbb1ecc9ad48777dc5527e4ac2a91c31738c0e4ea5508f2a6fbd842c3a72`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fffea151bda2665d2a326b7536585a8e9ce0c5db9f8a10774a9d9bca5cb27d8`  
		Last Modified: Thu, 17 Oct 2024 17:48:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:60b6c7c64bcefcd243ed197ed122371a268ef6034c07722c9c5fdb7a189d03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f3ec6dd2a45239a2c3a6bbcf6a9bc7b4b8a19459c11aed35056770330c51ac`

```dockerfile
```

-	Layers:
	-	`sha256:460a602c08926f1a69e6b40e07cf190b6e96b24bb8f0b6409031dcdf5d385690`  
		Last Modified: Thu, 17 Oct 2024 17:48:25 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:c2279673870eefd9658045996ac121123cc97c6c7766190ffdc6837cd9fc05d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee12b32353edf4c99929f0b0b0221b4e0e4f83471a4d8c07dc0b37548b5d6a0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6bb5cc70f20c4a11ac5a7b6cd1795f31404c38fdbdf8fcc938348116a1d318`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e8b81c63ed9c8bff907ec140e942f1f99f2c4a39d65d28fed2b30264b78f4`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.7 MB (2707181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25014d7743fd04a8253d96da7731e23f7b70629a1f354a990388ca26b44a55a4`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 1.3 MB (1323757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d0a9a1afb2e2a6fe7d56cef2a61a81ba8316023b20a73c1587c281c13bc5f`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946bf60c85536cab4d3e24d06d2a7602276812a054ec7b84518c322654aa57f`  
		Last Modified: Thu, 17 Oct 2024 08:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:174612b3a6a8a097a45dab376d430b4672dc9f93f6595dea7d25a1f954b083e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd90879abcb0f85256cd5b858d2c30d3c7c8e1866bf50f86adaab5465c5d00b`

```dockerfile
```

-	Layers:
	-	`sha256:f170a4333609467809bf5dafef7152ffbca1b38521405398ffbbeb12a3f5f6e2`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 2.3 MB (2285063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fc970f71e8a2e8b5b05ca0b42bb4917db5df7bd191b83db76344f56b249b0`  
		Last Modified: Thu, 17 Oct 2024 08:47:30 GMT  
		Size: 21.1 KB (21133 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:762d7ae83df22989ebffc9644e00373d07065f3d1d51b41ab1f3a4629eca7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280855a507271bf3dbd411e0b5af3135bbfd3e337e4fb25c10d0cfcc7a8f036d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8da1a3aea549bd7ad92c611f8ead90dbf061244fac1fb93f637bf5a7ce428f`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e5f58576b0343ff6a2282832e0b4a0bc58835b68d7133abe8cc53f980737fe`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.2 MB (2155824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5ce33725eae64b73eaa20d4cfb94a0c0e0587f2bb2eada7efaf38c095b148`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 1.2 MB (1237898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf8686b0bf276e5b26c69ad6410939c127d0721e86b667af6aa835a167aeab4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfcd584c2f7bfde09e56f6d22f82aa3403ad75f88b3e468d4c398b181dae43`  
		Last Modified: Thu, 17 Oct 2024 13:19:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:574bca1beabd7213b95f42e7fa4cc5aa13b16fd5e112d6b3ec7cbbc86a94a708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c923a5fdf1a9ae03bd4874bde2d4aee7501c0dac8b24445b7e998bb7157b37`

```dockerfile
```

-	Layers:
	-	`sha256:12eed464bc209f48cd98473519fa1ee7c8ddd317e6768f421ec2d8d5590b24ce`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 2.3 MB (2280513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ad9e3799b77befb0ee0f78e0e844e48ef284892b7f0bb74b2bcc0ef5ae2ce4`  
		Last Modified: Thu, 17 Oct 2024 13:19:47 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json
