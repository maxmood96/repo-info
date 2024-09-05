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
