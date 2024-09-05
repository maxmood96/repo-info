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
-	[`memcached:1.6.29`](#memcached1629)
-	[`memcached:1.6.29-alpine`](#memcached1629-alpine)
-	[`memcached:1.6.29-alpine3.20`](#memcached1629-alpine320)
-	[`memcached:1.6.29-bookworm`](#memcached1629-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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

### `memcached:1.6.29` - linux; amd64

```console
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29-alpine`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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

### `memcached:1.6.29-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29-alpine3.20`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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

### `memcached:1.6.29-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29-bookworm`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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

### `memcached:1.6.29-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:462ae4a35c26d8b66490856514c751651e63bdfd965742bbbe188fae79b32408
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
$ docker pull memcached@sha256:02a91acd281ea781c796f8e4542c4d1bfed38fc99fa56ab2f3968cd0ccf63620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c29b017628e3e7dbeb537c22bf018bc70d860cfdbcbe08129a4cbcd371e912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec3b85683b200ef7f73296e73a873c5c902d4fd7b16af3f54224e55edc2209`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79384d74e5b705884e9c9ae998d849c51572c54861284fff1c32a46ca6b8dbe2`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491705db671d80a4276c658d5e7c1418c693c3bf243a955fed250c7224fbb0`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 953.8 KB (953776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bfe37980acad5eeccc68f105e387d3cb851a20a83eb979d64b64af90507898`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988da8922e5c858be57ce711e11ab8c636b78c40399ce08be64ddf3e45e6cbb8`  
		Last Modified: Mon, 22 Jul 2024 23:08:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2d9ad35f1e2ad8763af603a8bcfe8bb0501d12ba8781a11be8af515e10fd0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b88871f138b31d495191226f22b8d7b77c70d163b2b4bd8923a177a6b06b83e`

```dockerfile
```

-	Layers:
	-	`sha256:0aec396d1722a66f6b534933e79ad1fd253ef97016acf64c97e26a83a6644ccd`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e9629bf53f8eb314880575845adca2c6af042e0760118521ab9d26f9920270`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:65a1d95207512f677ebcbd00dc8c5b86ba1ecdb463f6f39d5f336c65e56b0d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46d92887c374a71f70d2c39c9e1ef6c002c43a21c81bcd762048cecc52b159c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e766491c176eb516e5822704c8eed5745f64c968688dbdeecbdf154b05be35`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151424149628e25357b166643b1c729d6b95f9766cd1d0479b9c40332f82efb`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34645a165393c068c67ff3d408394b343bad79113d890481071364a3d9b45d`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 958.1 KB (958129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edc52e9ff916cffc4dcfa10bcb93900bfeecbc579717f41ed7cfc2289275c`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3884379460362a8b60e31a08da5b5b90743c581e887b3ecbbc9f85a8435e8`  
		Last Modified: Tue, 23 Jul 2024 18:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:da955547c573cf92f393616b0dea4fcfe0822c16b7309cded58dc085cf9bd331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca1f8d2aebbe85b0e1343bfb690ea8f98e8158ed61e58e1005d9b8becf951f`

```dockerfile
```

-	Layers:
	-	`sha256:1c3c2421b0062cbcbae3ace947dc4ced46de92232d6e7273e9ef19037ee29ba2`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48cb509d37963a6b4762b9fe808377dc727484808d2c258091ba0523cbee7a`  
		Last Modified: Tue, 23 Jul 2024 18:29:09 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:cb26deeba4bb0a69de1dd331ddea42b4b884d4597f131d481cf9246cdff60cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1d9146864c6f8e2690b20386a3f3786903de1054fe0acb31781ee0de57356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f44e107a92812fbadad79b5e65cf63c69934e8d087105feeaaf5301c4d86f8`  
		Last Modified: Mon, 22 Jul 2024 22:13:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ee7e9c13cd14384f22ebdbfec36bef4f2d9ddb7bb513a10037262d576b1d`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9538946247e2d8d5b622ee43b2e32c7ef3aea98e154d6295466b12b5a91433`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 946.7 KB (946652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b37eeb751c0361c08bed8d85ae9449c9902a9c24d2dd2b8595fe17098d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172489768f10377ada73a5caa3b5d582e4961f441fcba8c46315fc252032e37a`  
		Last Modified: Mon, 22 Jul 2024 22:13:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f60235cc648a8673f84bd771ff86126c5080096cdfd56f6c2272ee639ca14376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62719c0e7c1dcfefb9d2f221c54bce28120f0a23eff81a418b82c02cbeea32c3`

```dockerfile
```

-	Layers:
	-	`sha256:60402109ae73a83bdb214aba4e1a9419d41c3ef6a39712386af4efd0a54d5b98`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936d6aa69b908e475369645b8067e4c6e6cf534aa1f54eed1174125e4eb8f558`  
		Last Modified: Mon, 22 Jul 2024 22:13:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0999c166d942435f3000fdeff91150ca063fac13950a5351b7f6009032b22c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef73e0c8e6369a4d2b08ad9a71d998dfea796de78d9f98ff1dfc44c164e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8354009d53899d4f9f8a9cf68265683e708f0674c6cac9db9e52dc2b63a9b60`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f78b32522d89f523e8d952c178dd4fbc6227b81a9350ae510ad6af98bcc0bf`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 123.0 KB (122987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4473898d27a7522577b429514e8c848efd2ec10f2c526e3e7fb7f2c31fa3d219`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 992.6 KB (992558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623c015fb9b09c6e2a7e244739c0edd2ad647ae427fc278a183d2065c2843c7`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f134f1e9bb671e20240d53800656782d0d6636db50018b34468b8849793245`  
		Last Modified: Thu, 25 Jul 2024 02:51:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:034b2cea12997a66feec9c3cdf24690834f5cb53f89b6d81602a22fe458cf522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d282490b1580f0193880179f8d9388515803ee526744592953ec88bfff69715`

```dockerfile
```

-	Layers:
	-	`sha256:50a4d5c82df9b470fb52d5708e89e7bc882dfb0daff523f0c90d556cc2f4e386`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db61cdb75fa42df547d6d37ffb8e7096f73416b1d5217bb231e211fcc8ad80e5`  
		Last Modified: Thu, 25 Jul 2024 02:51:24 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:f7ab210c0e9eaf21e27262b8807fa854dbdd00b38a9808cfbab540c5147d16d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50770a03472bd05b025712db954615b8b6e99ef91fd3b522b3764b5d467a6ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd955a8f522eb52146bd9023aa32522be9e9b16678a1891ce379c0a0ca333f29`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff2e2e8a4e4a4c2815629a6e9021101840e4b9b1c959b342ec33bfea719d528`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 112.7 KB (112741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de1a92bf9806c7839987d6ee897ef80da1f3da08ead8b95fdbf85592dd0d5b`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 976.8 KB (976796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333bf980378ef767dd78c9575bc126fcd93d96237edd14f3e2c5c5271408103`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f4f9eea8d1f6d04bd48e17e37ce630ff26f65d09eebcdc4f96928498b9a64`  
		Last Modified: Tue, 23 Jul 2024 16:51:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:bc3139e0e3ce02c0c2171d7431e17195c6a8a8d0af018e5d9d6da44b9adfd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97b502655aec28f7870acbbf66140c06df1fd3c70521b86277aee34fed36c3`

```dockerfile
```

-	Layers:
	-	`sha256:85f8896f912ef4f9d12dc6386dacbc92db634a6483150b4321c37c2dd3b4f641`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2c1f4cd16f0ac1bc5775e53e7b72a9b64da072e74bf928c6ceb810bd1ac7ba`  
		Last Modified: Tue, 23 Jul 2024 16:51:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:56a39bd5c2d5c0a656d0aca25ad5b0d8cd40b7050d2805b58a04194a16d3953b
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
$ docker pull memcached@sha256:486b2361756abc71f40580014d23cf067c66c85b5cffa5529d7551adef824c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca8da22bc49d671df9bb785f74ec6874ff2fa1b953538fc79f07dad0548002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1cdb3d988387168044520aa60f62a2acd97412b207138299353e5d7e422e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed31f7e78c5df826533938d162a9662c45c5c14ee218b7dad0a5e4d0860c1dc`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.5 MB (2491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4dbb2094fb60b61938815faf28291dcec8f450390b23d2a17fda8e187f66aa`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 1.3 MB (1254067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89c539e7c021cb2ae601db4ab1f3e767f25ee3acc452a748fe55610f9e4556`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c57f52c45fd01338fc16c454e8ea91ea526384870db9fc151f8d1b38912da`  
		Last Modified: Wed, 04 Sep 2024 23:13:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3e5f09215dad51d68e0bef9b894b49c7ebf2c6e714bee0dfd7bd12409abb0a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3835fd89efdf36ef5e53eb3140ddba7c64a4256a5426fedc78ffd6c37ae849`

```dockerfile
```

-	Layers:
	-	`sha256:3af7b07fe2ff6024002172e7ef0e66e659c7f9de9ed8d2c5094dd167ff24baf5`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a16f6a2da5ca79f61eaa1685680694903adcee1fb741ef04c8272f14e2356f`  
		Last Modified: Wed, 04 Sep 2024 23:12:59 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c3f1da7e303581b2a85a3480182f12e248fcc639090229615d866f9660362c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30218311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfed15f8fdae6dfb0c6ffd0479e921174286f4b1ab0ed2cdadbd5daf36825b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed85fb416ea3b7af47a990f74eaab85545f0105dd38b16ad7724b4a38b90cdc`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d7623c0e8900bfe9cee340d97a7840c42e53150cc17ca45c1813b0fdb7987`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa424d1433cccf3fab49511efbd242f4ca584a902fd0a5150e7a64983c71c6`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:9163ee57c430e30d904ed07bc8da5e990591ed6a1de7a8279586c8e9cd7c4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51d83c9d26dedae5a6442d639ef4db7a8dbeae636f458b7e27d0c3d55c8312`

```dockerfile
```

-	Layers:
	-	`sha256:edc6be7451c0f0740c8318889c062dbcae6d94904239ff41b4c4d636bb3ceb28`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304b3c37ff7f570f4dd4ad1c2600932eefb14e376c2ddfae8a64109e22a3f40c`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c36e693efeb066d6108b164fa2de537c14dd638c20def735542128b70eaf049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32763935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4bc5941413a1bdcac522d43304cb7e2edeba60a0a73c015c0c6db899e690cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211ba36996a82c7c93bdac2efdeb71e0da593795c5258d8d89c033fe33940aa`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8c9b20da1a8b9ddcf199ca5a8e3f516b8a4dc20bb5207d36f4a84bef2658c`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.4 MB (2354827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68f968acd92c6bae0bbe52358f7ae2da75607713c14719508920b13122bfcf`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 1.3 MB (1251051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf6f357414f7f31fe91e25c79258ceeadccf2faf3d6ee3ee4b5a964e825ede`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bdfadfa32e5b9b8065acf610d804a7d1f979dd71aa95bb964ab5248d0bbb6`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bdc7f967727177a5f3a715451b4df5aa42694e1f90b8610d9a094c03236d8ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b1b2f65a985f35fbcc9c0e71472cdecef2b5328054ea39bb50082d5d07547`

```dockerfile
```

-	Layers:
	-	`sha256:ecd8e647c1bb123ecc2b18f42640b44e820944f14c9499ffca64c2001a39b440`  
		Last Modified: Thu, 05 Sep 2024 12:29:52 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ec0d1a905cf9eaf9906c2ef77e8a6eb0dd09dc4b35de52165570d9e2f869c`  
		Last Modified: Thu, 05 Sep 2024 12:29:51 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:8db7043b9ce5666f6b8a4dd946437b8e10e358e7ea56357caf71279420052056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33899869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957b2fce7c94bdc2fc531e22a45e9371640c8a3f61fa9db60b86960d7eb53139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae1afe997fdab7c196e7161edabe38fbbd304a8ffc60b2c42053c6bfd167e50`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06339446f764080a8c5181693284321f0ef0bcff75556122481921689df638ca`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fced9004b1347f9f945d8f590b7a6d82e7fe251ac6aa7b090907815b3e97475`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 1.3 MB (1254746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c30721691053e6b913794f1e30eb94192da7a55d3ffa35ef88bd5771b65a1`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd0d79030842bf2cfe88fbcf009da07a8c76b0cb1aae64dde8de0780a5999e`  
		Last Modified: Thu, 05 Sep 2024 00:10:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:46f57185cabdd9c3c4f5dea8f01bfe0b262d7a3c0dc5a704ba690f7dbbb49182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400545e80f6e89d605b7c02570a08d3dc33a21aa9023ecb70081a0afa2644bf8`

```dockerfile
```

-	Layers:
	-	`sha256:929c4e0a1980cce24f75eb1d55c74425f81496c056b8aa8ea512f38030383585`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1931d9eb7a7685e99d5dbe48e10961d18eee076e2c6acc82e166d05ea5d402`  
		Last Modified: Thu, 05 Sep 2024 00:10:47 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:9cc48022bf8c91ac93eef8557abc7a5c9570b5b5aa85e6091a9f8d2aafd5d20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32318911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67940ce2f434ba7eb6df985e0b4180951d5a874c0573d91d394d10427633a26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9e724139d1d990dc991e695a96a653101faedccfc8a08291ae64ea8b9b3cf`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.2 MB (1249649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c0da19fa20e0b9fc08ae632afa043159826fc3a4e3f430c8072e803f5a245`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2def17bda64a0d37af3ea7b9c3f84d69046f74b09c0ce72987b9c6ff5edd9`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e976f6a4636ffcf6c5a364902a5653a49e1941271fd564d03fcf52ad8e46bafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646883976e0caf986e1a40def65bbe359630acd24c6ac7c3d876db6c067d4d66`

```dockerfile
```

-	Layers:
	-	`sha256:c134dfcc46d0ae49bddef7d4f5776a4e8a8593a490fb58e92eac0361a721b917`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:e74912fd1b0d402b20b741cccf0fe00500a56512164bdf82a4e80bb160af0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37150902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb684f74729e122bf022802c4b6aa0e91779bfc25b8301b4c71b33ff4d464b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b901610c4a88556b291b061cd3b4a73d190192bdba453e55f6c1902934e383`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20281f2f981d417d9f7cb91ae9b3468134ea5e14e4b0211f795706713c5ea996`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.7 MB (2707201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135b41f762010cc19e097b3da342810c85ed1b83b009d519f3c204532868432`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 1.3 MB (1319832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bfc555e897ae93cf44e191405824f56ddaaf921ed1e79dc027ef51659a928`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9ccf1951082643c68304b82056964d4c37b5f066243cb8a453c406a71f72d`  
		Last Modified: Thu, 05 Sep 2024 00:43:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2b1bad6dde3648e3829945ca99816fba3dd91db19884b5ab8df7a1d1a30273eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec54c34b0427c5d9eb5bccda7a9cffae1ec61bf626255c429b4005c57c93eb`

```dockerfile
```

-	Layers:
	-	`sha256:b01747556115a27890911452943151f647c2510532c9ccb9c39a9b7b1cb0a823`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e1a086800183c9fa9da058fe52454144da8029e6f2089b137480d0ed809b10`  
		Last Modified: Thu, 05 Sep 2024 00:43:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:5ca93d243ed7d66c677ffc61bbb86fc8d92357bc67bafd0beb0f2f81abd2dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30881008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165923270842c0b67b32f6dc074d5549942d66c7c1ea2702fd3a7a5e8fd82b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57778e7f273fed2e7f39b939172e15edef160a99e95415b6b6880db7d1369194`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952a20973d5f6e5bcf18cf0480f3fe552f107bd49fb9197cb92dcee519a9ee`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.2 MB (2155804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84cc9dc8ef4d1cc2b0814adc2f45193d4e6a0a5250baa427344b81a02c882`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 1.2 MB (1233369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e2692779230e955ddde51898c5223a52597c0dfac97708b0feb8a526cf460`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa73a60c0b04b0a04f1af0cf87eb50584d077e7ee25efeb8280246c08b03f2`  
		Last Modified: Thu, 05 Sep 2024 02:49:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:18669b0153cea7380b6724af4b12c8ea8a335bdc2dd5a320d7b3df35ec4ea907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff573fbf2cc1db42a95238879b0a0dc57bc098d8f0989002e2050ae5a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:17a7086a8728bcd134cb03e8cbd6ae42f5e73f2b623a8fd9b0c5fcfb65d1b72e`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489539b744210b0155e45a4c48ea616896d21e87fe30792ad5d642b127125aeb`  
		Last Modified: Thu, 05 Sep 2024 02:49:19 GMT  
		Size: 21.0 KB (21027 bytes)  
		MIME: application/vnd.in-toto+json
