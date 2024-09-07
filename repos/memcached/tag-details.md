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
-	[`memcached:1.6.30`](#memcached1630)
-	[`memcached:1.6.30-alpine`](#memcached1630-alpine)
-	[`memcached:1.6.30-alpine3.20`](#memcached1630-alpine320)
-	[`memcached:1.6.30-bookworm`](#memcached1630-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:508f8310791bdc03f5a96e1b665c21ab87fac2d8a5ec6ad4430ae54b50d6ec04
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
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
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
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:508f8310791bdc03f5a96e1b665c21ab87fac2d8a5ec6ad4430ae54b50d6ec04
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
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
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
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:508f8310791bdc03f5a96e1b665c21ab87fac2d8a5ec6ad4430ae54b50d6ec04
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
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
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
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:508f8310791bdc03f5a96e1b665c21ab87fac2d8a5ec6ad4430ae54b50d6ec04
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
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
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
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.30`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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

### `memcached:1.6.30` - linux; amd64

```console
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.30-alpine`

```console
$ docker pull memcached@sha256:827825cd046a6404ceb88be551f235b33d43162a69f1661b949267627d76adde
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

### `memcached:1.6.30-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.30-alpine3.20`

```console
$ docker pull memcached@sha256:827825cd046a6404ceb88be551f235b33d43162a69f1661b949267627d76adde
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

### `memcached:1.6.30-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.30-bookworm`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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

### `memcached:1.6.30-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.30-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.30-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:508f8310791bdc03f5a96e1b665c21ab87fac2d8a5ec6ad4430ae54b50d6ec04
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
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
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
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:508f8310791bdc03f5a96e1b665c21ab87fac2d8a5ec6ad4430ae54b50d6ec04
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
$ docker pull memcached@sha256:5accfa177af24bc2de5fc5929bec7cc3e23e301a42ac81f8dc2a66816bc39368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d6da6a84fd47cdb7938bfbb6a982abe5ab2d965712687cc2a14feace74e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4b84fee68b60411afca6e812eea63651ac4317abad5d86a4a7453bf272c4f`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f425ed6720deaa6aa8f6014d2a3ad6e30e18861c2b947bd07386a09850dc2`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16513724c49b5f1bc7176fa154d51030f0c354c3984c699fba31759043532b3`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 958.8 KB (958784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557111eb5fe217237ade17f0b8b872a08f719618e9674ee89a8a24b06e54291c`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e491162ccb9db28b06f736a260cced0f749e2dbee7f57b5ed9de74cea8fdd8`  
		Last Modified: Fri, 06 Sep 2024 23:25:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:954f12a89f8d9e1bb1db7bc8305e1d17bc766a10c328342680582cf45e945b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cc8835ff8b9956353b878ec165a3e511ed733f49ae30900dd4d168f20575b`

```dockerfile
```

-	Layers:
	-	`sha256:7683ce1c0c218b877a5caa1607dcee9686778e3fcce3064ed848faf9e50f6624`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4677fcfbaa603cac216f5d2572827775c1d790e32296c5c25105e732c310ba0`  
		Last Modified: Fri, 06 Sep 2024 23:25:09 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:43d1ab84478cc075c86e48ea5bf60df8771136de6f02bdba70c1b3633baa9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a53222faa796471f72cce98e3abcfa4ba6fc43c77d3686099ecca87bdbca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0287f626b30250c9b50fe604a96d50c1e17c1f4cba39418ae49040dd80c8cb`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb24140b8e0cdde5e037f635918a49810f651ec6c99ace904d96aee223c64a0`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 109.0 KB (108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6568ad942f7ad59fe322deb60dfa6a00c7f76766ee56c08723db9e5f49abc6fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 951.8 KB (951810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b8f4693c44008c33cff05c2c63738a2fcbe6d64127a1cde9be5a55b7fd49d`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebd7c3af00eeefb20296ea0c2e15b464ea657883faf86679b50b214ee5e313`  
		Last Modified: Fri, 06 Sep 2024 23:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:adb64838d510c190429ff27bc4c4e191f43a4865f73ba8ea03482061bdb927c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861914f38853df7e7df60ee0e0912ed5a66e878ce013476fd114338a0aff3e55`

```dockerfile
```

-	Layers:
	-	`sha256:6334383267618381955f719ffc085ce41f292e9de6a089757d2eb1837c6fa84f`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e41d7009371da42bd3017f09b80be5a663ac296d2c2fa11ddc281cc0c2cfde`  
		Last Modified: Fri, 06 Sep 2024 23:25:16 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:c0337f5f939a65cf2557d236cb2242274d0540c83a8c8eeafc3badbea4e8f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6208bb1c249226473b9aa3615c59e49f09b147e8822e6bdd0ab74693f823a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:dd3d84ccea40eebc1d3f73f4228d7e88eab1f3db0b79e9b18f6842433b4ea922`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 997.4 KB (997379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114c611a1ad745eaa115355d5651c4459e63ecbfc4bf4552c0b753a6448f483`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86eb6c26e775dd0cdb814c61b45def56112ff869ac76b622df696664e311494`  
		Last Modified: Sat, 07 Sep 2024 07:05:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:041b59013a298233807f685393c3421a32bb5a02950520fd9eced0b42c5f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d357371a60348d05d8fce4d7a1d84d14494bd32b1e4184c2ada5a824f837de6`

```dockerfile
```

-	Layers:
	-	`sha256:1cac78dfe8a5cf3b8a02cf11824678fe827121b7372af19704cc416d26c18864`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ab8a1ff8907e3a398b58f3f981222cc2071cd09afa6340b63b3c0162b4d573`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 19.4 KB (19416 bytes)  
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
$ docker pull memcached@sha256:fae9f484fd616c5d3c8ff6ed664b2e387eb26ed7c7fe0ae7a1ac4f105c50e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc201daec92aff2b1c6f2ec544334858e5a09cf9a144b98eafd82e7dafe38759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:445595506fa2a09593db5287ae74e1ec386e17c2d3e0344d2fad562c873c4265`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 980.9 KB (980913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c627abb6239cb7bdca492eedbeeab6789ddd9f11346dd61b1dbc26f571345a`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa9f4f084d2ca4719acff9b915ce09603423874298d6b6667164f5d4a63d278`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:677610b98bca3491ad0de7d7e7d0c4c7b2a1bbd2cb12c6476495b0da34c5c633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87922d95cd2a7b37b85391dcfb63849b985d76f46f00de8abc218ce6300dc6`

```dockerfile
```

-	Layers:
	-	`sha256:9976f18f83ad09202aa5daf66d787c78d3af16193eb6b19b2ae9898d15176496`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb9b000a566f33ab68678e361e2c0acffbe30ac287458012b1e69e2cc44bcb7`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:618c0b453fe1b3a02966e2cd448e8bd0ab60d76212b2ce884664766a397cd402
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
$ docker pull memcached@sha256:13b2cf5ec4f6d6858febc003d88bdbf9bf28edd292e97fc7f8ab2a4751c10df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07de26c710d6e053aad706ede2269ecaaeab5a9444854a06dfef8fd2937ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35766924a4f7039fd4e27dea4dfb947ce9cb3dedbf8fabbf399e8b9d422d2b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580ca8a1cdbc8da3bb5c24917290b152a35ba989b445a3e6bff51cf00d9e7f8`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.5 MB (2491323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4269e8190a40cd532ecc7e2faa934c31544fac68478c7a22dee76b110316e`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 1.3 MB (1259238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e99d3083b723e1b53cfcd401983c912650eb903a303c04d878bc5714e311`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5279091df43e679cfd7c916a765f9ae9312d1eeddaa0254fa1dd74a024c8954`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5b64282ca15138b6d35cc90ee8573bbf3995e2fbbc1e4e8434ec5c244d23e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c83457267377ed6577bd76696c74c6d415aa13df82e1dea6677111b88818`

```dockerfile
```

-	Layers:
	-	`sha256:9e0f21555c15c7c8fb7b0f2dccb203091919ca214ec2a91c164970ee8c6af993`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf2c69b4a169f8f61cabd34a2a96996616f7b52a2cd72dd4a775f673b68559`  
		Last Modified: Fri, 06 Sep 2024 22:03:50 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c048fa0883787788b0c022ae57415814e449935245a3696f3303229921f25668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b714677ab3f358c1ef046bf331b99c2ddbd9a25dbbb8802a5b172f5806c8bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:e6117aa031ad0d107e0d68adc7496c4031e7d07329497cf5650af90f8ae82e66`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 1.2 MB (1238266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ffb6ec1a5ebbe16bf5892b22bd5bc49bef063f277c0ca085bbf402feb7d9b`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ce56863b836219ad9b528b916dba3b8d8491848787749bbe0b2802040dc9a`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:fa82b4bc0f4706040d334f6cfca13d6342736e1282b23478fe34c91fb9efefff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39184466563e3c51c6a223ae7ccdfcba42c5c355ef4b780b8b1e0825864d3f0f`

```dockerfile
```

-	Layers:
	-	`sha256:257e2dd08192402612e6a07ad0349f1714c3188aed92729bb20faeadb1362431`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138a59b44a2ee2e49068d2732f4dc09be7e8b49cc05775e1feff34f78bfa156`  
		Last Modified: Fri, 06 Sep 2024 22:03:10 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:3a7ee7a7b47cdcbc24692668ee6787d840f14b26401342d1462c491a3db97ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad06a6d3a51286adf479468f54d0db6376b2bed5689792aae2ec2f1133046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a5c863c5f1d3f7e4473dbb43b459edec53cfa121a0caf6e921e4168f256d65`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f9b092e9fa77b41af32fbfacd661ef3097140d5fc958a0092e8a71014b4f4`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.5 MB (2499321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1759f94541552eab8f9a547ea7f652b18acd1f1714b7aaf0e727155a39a269`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 1.3 MB (1259403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577ba1b11013532b83f3c1c66179d47313f5c148c5405930b55e1864470fb08`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c36be08181b9b51a9af475d109a8350e222526535d64767b36bc6247e052d`  
		Last Modified: Fri, 06 Sep 2024 22:03:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1c029c31a6b85a6677946931c62a5c41c75480b3f4fddb8de7656458d7ad0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b2d7092dbf829006f7e996b4395f52ebaa1047a2d5c10787af1679acfb66`

```dockerfile
```

-	Layers:
	-	`sha256:ab588dfa4e7c500e00a97054e30528b8eacd637754967a4cac7e99c7e3f7434b`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63174ce7f6335d43802176174ccc1e7946d569844bef297145340565f3d081d`  
		Last Modified: Fri, 06 Sep 2024 22:03:51 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:b2cfc14720f80dcc5211c1e2d37223947554fd6e980ef49307bf8526bef3e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6707680ed8671f7fe1dd49304b69b54652fff9873d6d95755791492f8690f1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:75f246479ecf3f7c1fd5a5a53279029fd89ea9d30f9bd4593645e20d6a026dca`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 1.3 MB (1254322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b72d1d0a079be6a20ae7edfa829462a042acbfc11f53ed86c24d107cd5d41`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d94f331381eea15b342c7c5b7c1d009569c89a63f09fdb311e97dc2aeaedb0b`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:66f71299408392c4e7de49c65cd4a35ab9711e08105aa51555c996811fcbe66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0377cce6aa7ecf26e78b7912f5cdafc59660a80d8aeeb5f07da507bc11715`

```dockerfile
```

-	Layers:
	-	`sha256:74671384b3e8fccb72dc24be71fc53131f7c2b9e77d45d7d19b508c40b3e0297`  
		Last Modified: Fri, 06 Sep 2024 22:18:19 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:f1d4af1ef6277f8a8d20d524c7721b3c2db0f2c410cd56ad3a91f954d9623491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf90b687fab7c9a35dc6ab9399b565fa0047db6aae3477b1ff378e282293c8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a8e8b7ca15295540b0362c3e51115c5459e1a7c1c50dd0409203e5f67f5f8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.3 MB (1323732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f1aa14b638afd657399c79d3a44f002fe63afc5e56253154912a0fa6f476f`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa39e993af3c94b36b283aa63d3ee230e2c136d626cbc56fa5f1a40ecfcbe`  
		Last Modified: Fri, 06 Sep 2024 22:02:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1ed1d2c2b04d3f0560f1a72a4061dbddabb5ebee8d83a017e85b948a1001c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a57137331a83c32d713c3f56e5af68f407ce4536101c450dc13de7e8bc5054`

```dockerfile
```

-	Layers:
	-	`sha256:81c5c10c39ed3d1ba865b3a07d16aa8cdad615d19e74bc7290c1b5a46d7715d8`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9c393162efaf6073047de0f1a987580b022c8a1be429f534a8029a31e1d03c`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:6d8ffbf8eef02adeaeacc2a70421d61d12f6e44008172d9be3082183cd51bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123f963d79237102a6b54e8760687b1d89da2372197da309829075c17ad1408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17cb87477894b2b6e9dfecabb463ba0b8e16520f66e49e5f48e6de785d646`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.2 MB (1237863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4225beb9612c03f131bcf18d4a5e10c87eadfa1a4427af71010a6f90c4d77f`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39acf871d9b4dae7c4c164f718ed3ef3147259c9c5dc2450815c38e9d66a562`  
		Last Modified: Fri, 06 Sep 2024 22:03:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f1b46417c05084a5d49bbd0892d08aad31090c13217d059768f3908a1f8d091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f67aa8e0dbd8c2987753568e1eaf27ecdf4da962bc0f91de0dec3a10595231`

```dockerfile
```

-	Layers:
	-	`sha256:54a7ebd3f06bbe6c94615cd1df020315450a6854a1be016370087b7f26b93b7b`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac94d07a3de8056121d03f2e1aa0fc3b3ef5f56a7abfb6f4d0b89a39e1df671`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json
