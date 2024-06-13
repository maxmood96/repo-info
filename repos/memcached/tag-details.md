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
-	[`memcached:1.6.28`](#memcached1628)
-	[`memcached:1.6.28-alpine`](#memcached1628-alpine)
-	[`memcached:1.6.28-alpine3.20`](#memcached1628-alpine320)
-	[`memcached:1.6.28-bookworm`](#memcached1628-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:1.6-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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

### `memcached:1.6.28` - linux; amd64

```console
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28-alpine`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:1.6.28-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28-alpine3.20`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:1.6.28-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28-bookworm`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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

### `memcached:1.6.28-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:d4d913aee30537fea2f970892e2e6f901292d07bbbb088414ea746abe21d970c
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

### `memcached:alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e1c337b160521ebd662320806748d3096129d0bf58ff09729fdf34cc62540ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f516946baef121bbd8c20888557da5f7dfe672f3152aff042349e1f34c64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba03fab7b7a6d8d9dcb63e9fe367fab6421cab7d062d5d21e77d85843508fa6`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df432784651fb43b98d5af6e839218f6ed47b40cb19e8d7366b7f2c57ad47c`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60c8169be3fd72927221f9968e59947a8ac760244b8dd8c53a494cd5647f46`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 958.9 KB (958856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537ffe5ce2a1cf2bec3656c52583f406914add372fe527a5110d133dfeaf457`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be371792b4f987689681c25eab17545e94ccc9ac0c61d5d7ec5a4aa1393af19`  
		Last Modified: Tue, 04 Jun 2024 07:56:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7d021c55167e50bca78c22f01c0fc78e1dc30f36600627760a282733a3b38256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 KB (104020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9424b1b9259e1cab453115a5e6c236ad46fb6d9254b3a223b2c108e3297c217`

```dockerfile
```

-	Layers:
	-	`sha256:658438200b024c3bb30a9e480d3e3ca822781117c8d011d378af56e78e421439`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 84.4 KB (84371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd3db24fb9dee45a5b6815ebcad56c5f428563ad1bfb92cf30e388dc5ae4055`  
		Last Modified: Tue, 04 Jun 2024 07:56:07 GMT  
		Size: 19.6 KB (19649 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:63771cec6fd69e44531b570b01c9344e5620949cfe73a71bfa90daefaebe8d01
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
$ docker pull memcached@sha256:057168c5723ebb3e8633f6db20a9c20a972d9fc4ed61264ad2acbe9d38f9aabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b017b8ec9ca36c5ee88f85570db22d31a863b9e189a5c5684673c18565384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462ee6a04159ecb897a6ec67e849fb18dfb2088f53b5e632edb3d1608030f3b`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadd515705c234ddab2984ebaf51fe1761f94a3b5c03aa9098d3c0dc669fcb6`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.5 MB (2488515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f43f84c44021ee7e9f78d4d2d2f178f4db927b04f7224c0111665e4f6d410`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 1.3 MB (1257578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc471a8612f09ad8729ac1b30eca96e24c483bc307ac37a7ca8f53c65b7aa751`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24a632a1c5f5c42ba835e56726dc3bcfa2f18348292cdb637be1e8a1c9aa62`  
		Last Modified: Thu, 13 Jun 2024 18:32:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4587113f348cf385bec49f6359cbe1a29caf7d0e8abe6f4cb82750561f754592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff251bd4c6ad1e9c6ad66f1d11ece923b1c2c4aea9ba4fff424580c2e51246f7`

```dockerfile
```

-	Layers:
	-	`sha256:b0951dc5ecf1a3d627b5b6d0a3d82b2d26c838b8e40a20ba0383b75cee7de70e`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3c7100ca0b9247b6ea00d23deb1dde9e4b6cb98f8c3573b5a380c3563bb48`  
		Last Modified: Thu, 13 Jun 2024 18:32:20 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8d621d1ac5975a703df97d2599188c9c3cb15bde6eb65229944a1cd4eb60bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7aa424f84cd5c6512496f0b972a512bbdab12bf9d3666ffe6f9731e64c196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40160bd3d7a5b1af3bde3b9881cf46c5673838f467cf4d82be9f5f0443cc432`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae315d6a0c14389f69a2eddf728a5cd601b2fff9964e2ebefada90f9ab2089d`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.1 MB (2089509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e02c2879dd697603afe2a420cfdfebcdf6efa9179fc28490e13ff2ce8bf57e`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 1.2 MB (1236714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4414c5e808f3d762cfe7bcad4639fe166478fe1c42de37ca9535fa1c89e5689`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5c7a8527b817792c24d2f301ece6b685db819292cd330c9be80e5758ff856`  
		Last Modified: Thu, 13 Jun 2024 15:28:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b834f00560d711ae89cc16d1e50af295b5a80b72a952480b5de17d291ae7ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a330d2f7a03f9e0b096c6df642fa20b4847c37486f48738ca3ac11e85c97c5a`

```dockerfile
```

-	Layers:
	-	`sha256:868ca99518a369ccfbaa8a64ed1c26b109d075288305efcb436000f2ef45185a`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04ad52943fb52921d1d1f827180ba808d27c31c6424c73dc8292f126ba092cd`  
		Last Modified: Thu, 13 Jun 2024 15:28:31 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45dd3d82073f96baf1e169be23aa620642f1664b0ad1ec67c993bbf80f590806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be0ad95f78b7ec63d80b47829382f15c5cef683ac4373d9dc303bb83c2e4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9d9682b9484855572d2925d7daad67c1f742785f485064b590bd6886ce85e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f2b5eec704882a30399ff4a373e752d68ba2f8115c1f48c5c55bcb41883e`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2346195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d7cf80a3d4ff78ac30adadf2786fac76f79b9410bc0f2ea4c0fdf11014ee09`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 1.3 MB (1253936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41520a17d7e58b7009e13dd1e4d2a236e783e12151d31dd907982febb0eba6f2`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea7a2945f5b7c85b5c329d374a3f502dfab001e9d4733f5269760394c13236`  
		Last Modified: Thu, 13 Jun 2024 19:29:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4081e3cf43a64196d74fd6db038f6fe5527ccc8382df267aa540d74d6a12f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3c9f25363498bb0d73c45013aa544d731575fe6dca6f833727d031915de8e`

```dockerfile
```

-	Layers:
	-	`sha256:585e69b12038eb0ea20c6c76cc2ec34b6f7fed0289337dd2d965fc13b8792ffc`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 2.3 MB (2261574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39e3aba43496aa9fadfb8a406a2b7efc3b13e3a22199e55bd787554eb152664`  
		Last Modified: Thu, 13 Jun 2024 19:29:29 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:7971ce530eb22ce488a625ba4e1628744d7476c8b2edbe9f78e6be580fe7f041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad2f9e97abf7b296ba262cde8a5f46503ef7e307b2996838efadeab8fa44dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07253ffaf183562aa29bc7bef7bc3b4960336b0b998d90c035e2fa5de31e913f`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de4ff6a12dc045889bb909328015fdcc77773564de91425adfd86b9fa5495`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.5 MB (2492699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5589fc47b826a8a6a47bab3d95c6565a18db524f497a012405de6b9409abc`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 1.3 MB (1258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87123dcb34170129be7d829c61a7b6fe5389bb271da8e1c7b2385813c9deb4c`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d368703e953eadb00169f1fc3f63943ba52518f8807ae83826c9ccfb946ea`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:30f1068b6226d035a32fbd8bbe6aa1540b0b892ecd94a2bf5b0d4b3643cb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec24007d9bd367a18df95742be3c9f944c7b3c5c683d6dea68a60e733dfda40`

```dockerfile
```

-	Layers:
	-	`sha256:1b905f5580e30fe69d8caa0b8bd9542c801b61507deb53c551a7d628948f7aad`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef31a3fe17cf4eb135c91dc01da1d2afa004b55f542a36eaa4684b767eb84e7`  
		Last Modified: Thu, 13 Jun 2024 02:02:34 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:ab4bea60bd27a840867a2ce5ea3a8f077696bcfaadbfeaa12aefacd17dc38c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3619e0951231f3ccaff305348b1bec54559af0e32ad8c48611d3df2b1f908fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7963a68a20274a90728eb7b71809e0c6952954e4bbec249cd197215574c865a`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d0443070731d291cb6fcada7d9a564ba6be811d78de51ace395c34739887d`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b7b0bce8e55d270eaf8add9ef2b12c58454daad99274fd84c91e33460f6c81`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 1.2 MB (1236826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d83b29e0a091a759940849c94e6bfa91d044aa24b90abbb125c65d801f6d6`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502d901b7510365cb27fa94ab3361aed97f09b31fb1d0be2f1941f98fc266`  
		Last Modified: Thu, 13 Jun 2024 09:44:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5dbc65a3e4d8a93267426c236b5f251268bebf06a03251aa864e35dd45d61a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f4dcb9c347f72336725093081549a098d96fd9a804453094a9c36406f5551a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c17f2643c7d1a70b21068cc8af34d38ae83dd6ded47950135cf152931d82f`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9306348ae9be70d38556829527badae72196b6e7a8dd18bf81dc3275a2ddab31`  
		Last Modified: Thu, 13 Jun 2024 09:44:16 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json
