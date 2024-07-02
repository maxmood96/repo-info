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
$ docker pull memcached@sha256:99350c3328fe9ab8c2c62b304100817e06db1883743af824d5d790cfe4fce258
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
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
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
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:9e0c77bc2592abf62bc2cf3ae42e9b922e966fd2d3f341b14e9daa16ae71f024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32336031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534df337ea9166611422a9e058d850623b1749c1a9846d287eb0b8b3e33053e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7909e1f7ac0d00445b2eddfec259336a5b57ef7d9c3c258968102dd19c6571`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c132c075bdb41a15e13ba12da7727043533dcd509f6b3c40ce0631ba78a3dfd5`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.9 MB (1937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afa6dbd1e2fd2ddc5c2c53d2dfe064505604c7bbb8752542ba7f6f05a95676`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.3 MB (1252996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71988b5aefe34ce51c5e853d041329cce96e191f83189af1078d89dff84c5c70`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23505095ad5510cf655e5a06b22abe66a69cb4b8ada3191ebed3ed083004eaf`  
		Last Modified: Fri, 14 Jun 2024 00:19:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1428f0f6cd3f8db559d5b911a5ce48a2cdcf086e3cd560fc466a1942596e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d207c0879b9e33e8884fd2ce7b6fccc9c2090971a1a5d1b425eaaa1f2d53`

```dockerfile
```

-	Layers:
	-	`sha256:0ef6853745dbda54a007383832c9eab98a44361f2001fc3b3a2f9f224e05a746`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:4fcf7d4703e9804740cb368c205a56d353942a372564b34b85beb85afd430c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37164129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28a3f4cfda917b0c3a6e9eb919abb1a231e22e2411496f8091af07840b1e71f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855a9e32c179482484e2ef5ffc17445bb57ecdd08e7443eaf8cda621f379737`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb232fc864a5d885f4fb1b20ab634ec07471c1ca7d43ab5c6221ec79c03786`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.7 MB (2698425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcba21c1ceb62fdba693aaba8e20c36e599edaed883b605d8609ae5e33af31`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.3 MB (1322991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6a53eded239d055f27715b3b49d5d3a23a44a8b9597a2e05c9e0e22a83235`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530491c4ea43b457dd3b0ef88072d04ff9408648be3eec6a5ad89da9c2f23372`  
		Last Modified: Fri, 14 Jun 2024 00:50:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6a618ef6732e315dd52681d26e1fca1eb4a87b4786e29de103c0294d2cd77237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f114c22d73533b1f96b04ad77e637292c820f5805b01bd86a95d91086ed67`

```dockerfile
```

-	Layers:
	-	`sha256:65862383c3cf61bbe9427abe06e1d99e9a352aa8d3fab4a51596f03e311de608`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8483c5e4f7ee2946118c339543ebbaad7e1ef986db3e379b5989e22cea5b5070`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:99350c3328fe9ab8c2c62b304100817e06db1883743af824d5d790cfe4fce258
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
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
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
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9e0c77bc2592abf62bc2cf3ae42e9b922e966fd2d3f341b14e9daa16ae71f024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32336031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534df337ea9166611422a9e058d850623b1749c1a9846d287eb0b8b3e33053e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7909e1f7ac0d00445b2eddfec259336a5b57ef7d9c3c258968102dd19c6571`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c132c075bdb41a15e13ba12da7727043533dcd509f6b3c40ce0631ba78a3dfd5`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.9 MB (1937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afa6dbd1e2fd2ddc5c2c53d2dfe064505604c7bbb8752542ba7f6f05a95676`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.3 MB (1252996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71988b5aefe34ce51c5e853d041329cce96e191f83189af1078d89dff84c5c70`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23505095ad5510cf655e5a06b22abe66a69cb4b8ada3191ebed3ed083004eaf`  
		Last Modified: Fri, 14 Jun 2024 00:19:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1428f0f6cd3f8db559d5b911a5ce48a2cdcf086e3cd560fc466a1942596e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d207c0879b9e33e8884fd2ce7b6fccc9c2090971a1a5d1b425eaaa1f2d53`

```dockerfile
```

-	Layers:
	-	`sha256:0ef6853745dbda54a007383832c9eab98a44361f2001fc3b3a2f9f224e05a746`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4fcf7d4703e9804740cb368c205a56d353942a372564b34b85beb85afd430c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37164129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28a3f4cfda917b0c3a6e9eb919abb1a231e22e2411496f8091af07840b1e71f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855a9e32c179482484e2ef5ffc17445bb57ecdd08e7443eaf8cda621f379737`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb232fc864a5d885f4fb1b20ab634ec07471c1ca7d43ab5c6221ec79c03786`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.7 MB (2698425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcba21c1ceb62fdba693aaba8e20c36e599edaed883b605d8609ae5e33af31`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.3 MB (1322991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6a53eded239d055f27715b3b49d5d3a23a44a8b9597a2e05c9e0e22a83235`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530491c4ea43b457dd3b0ef88072d04ff9408648be3eec6a5ad89da9c2f23372`  
		Last Modified: Fri, 14 Jun 2024 00:50:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6a618ef6732e315dd52681d26e1fca1eb4a87b4786e29de103c0294d2cd77237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f114c22d73533b1f96b04ad77e637292c820f5805b01bd86a95d91086ed67`

```dockerfile
```

-	Layers:
	-	`sha256:65862383c3cf61bbe9427abe06e1d99e9a352aa8d3fab4a51596f03e311de608`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8483c5e4f7ee2946118c339543ebbaad7e1ef986db3e379b5989e22cea5b5070`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:99350c3328fe9ab8c2c62b304100817e06db1883743af824d5d790cfe4fce258
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
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
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
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:9e0c77bc2592abf62bc2cf3ae42e9b922e966fd2d3f341b14e9daa16ae71f024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32336031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534df337ea9166611422a9e058d850623b1749c1a9846d287eb0b8b3e33053e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7909e1f7ac0d00445b2eddfec259336a5b57ef7d9c3c258968102dd19c6571`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c132c075bdb41a15e13ba12da7727043533dcd509f6b3c40ce0631ba78a3dfd5`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.9 MB (1937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afa6dbd1e2fd2ddc5c2c53d2dfe064505604c7bbb8752542ba7f6f05a95676`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.3 MB (1252996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71988b5aefe34ce51c5e853d041329cce96e191f83189af1078d89dff84c5c70`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23505095ad5510cf655e5a06b22abe66a69cb4b8ada3191ebed3ed083004eaf`  
		Last Modified: Fri, 14 Jun 2024 00:19:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1428f0f6cd3f8db559d5b911a5ce48a2cdcf086e3cd560fc466a1942596e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d207c0879b9e33e8884fd2ce7b6fccc9c2090971a1a5d1b425eaaa1f2d53`

```dockerfile
```

-	Layers:
	-	`sha256:0ef6853745dbda54a007383832c9eab98a44361f2001fc3b3a2f9f224e05a746`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:4fcf7d4703e9804740cb368c205a56d353942a372564b34b85beb85afd430c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37164129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28a3f4cfda917b0c3a6e9eb919abb1a231e22e2411496f8091af07840b1e71f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855a9e32c179482484e2ef5ffc17445bb57ecdd08e7443eaf8cda621f379737`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb232fc864a5d885f4fb1b20ab634ec07471c1ca7d43ab5c6221ec79c03786`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.7 MB (2698425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcba21c1ceb62fdba693aaba8e20c36e599edaed883b605d8609ae5e33af31`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.3 MB (1322991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6a53eded239d055f27715b3b49d5d3a23a44a8b9597a2e05c9e0e22a83235`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530491c4ea43b457dd3b0ef88072d04ff9408648be3eec6a5ad89da9c2f23372`  
		Last Modified: Fri, 14 Jun 2024 00:50:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6a618ef6732e315dd52681d26e1fca1eb4a87b4786e29de103c0294d2cd77237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f114c22d73533b1f96b04ad77e637292c820f5805b01bd86a95d91086ed67`

```dockerfile
```

-	Layers:
	-	`sha256:65862383c3cf61bbe9427abe06e1d99e9a352aa8d3fab4a51596f03e311de608`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8483c5e4f7ee2946118c339543ebbaad7e1ef986db3e379b5989e22cea5b5070`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:99350c3328fe9ab8c2c62b304100817e06db1883743af824d5d790cfe4fce258
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
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
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
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9e0c77bc2592abf62bc2cf3ae42e9b922e966fd2d3f341b14e9daa16ae71f024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32336031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534df337ea9166611422a9e058d850623b1749c1a9846d287eb0b8b3e33053e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7909e1f7ac0d00445b2eddfec259336a5b57ef7d9c3c258968102dd19c6571`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c132c075bdb41a15e13ba12da7727043533dcd509f6b3c40ce0631ba78a3dfd5`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.9 MB (1937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afa6dbd1e2fd2ddc5c2c53d2dfe064505604c7bbb8752542ba7f6f05a95676`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.3 MB (1252996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71988b5aefe34ce51c5e853d041329cce96e191f83189af1078d89dff84c5c70`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23505095ad5510cf655e5a06b22abe66a69cb4b8ada3191ebed3ed083004eaf`  
		Last Modified: Fri, 14 Jun 2024 00:19:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1428f0f6cd3f8db559d5b911a5ce48a2cdcf086e3cd560fc466a1942596e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d207c0879b9e33e8884fd2ce7b6fccc9c2090971a1a5d1b425eaaa1f2d53`

```dockerfile
```

-	Layers:
	-	`sha256:0ef6853745dbda54a007383832c9eab98a44361f2001fc3b3a2f9f224e05a746`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4fcf7d4703e9804740cb368c205a56d353942a372564b34b85beb85afd430c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37164129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28a3f4cfda917b0c3a6e9eb919abb1a231e22e2411496f8091af07840b1e71f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855a9e32c179482484e2ef5ffc17445bb57ecdd08e7443eaf8cda621f379737`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb232fc864a5d885f4fb1b20ab634ec07471c1ca7d43ab5c6221ec79c03786`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.7 MB (2698425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcba21c1ceb62fdba693aaba8e20c36e599edaed883b605d8609ae5e33af31`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.3 MB (1322991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6a53eded239d055f27715b3b49d5d3a23a44a8b9597a2e05c9e0e22a83235`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530491c4ea43b457dd3b0ef88072d04ff9408648be3eec6a5ad89da9c2f23372`  
		Last Modified: Fri, 14 Jun 2024 00:50:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6a618ef6732e315dd52681d26e1fca1eb4a87b4786e29de103c0294d2cd77237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f114c22d73533b1f96b04ad77e637292c820f5805b01bd86a95d91086ed67`

```dockerfile
```

-	Layers:
	-	`sha256:65862383c3cf61bbe9427abe06e1d99e9a352aa8d3fab4a51596f03e311de608`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8483c5e4f7ee2946118c339543ebbaad7e1ef986db3e379b5989e22cea5b5070`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29`

```console
$ docker pull memcached@sha256:9fee354f31d4273e2310277acb9329ea537a5eaed3295e3ff054dcf9a1cb8e9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.29` - linux; amd64

```console
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; 386

```console
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29-alpine`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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

### `memcached:1.6.29-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29-alpine3.20`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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

### `memcached:1.6.29-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.29-bookworm`

```console
$ docker pull memcached@sha256:9fee354f31d4273e2310277acb9329ea537a5eaed3295e3ff054dcf9a1cb8e9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.29-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.29-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.29-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:2a48cbdaeec8c3d2a04f846db730111201164cfb8dc317089b8d801c4a0fea1b
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
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:27f78e66055216bebd3d8a8cd26916ebb5d707a297ff9e69a227b7069bd0c4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7859505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c3d1472f5d7253bea39e6e41d7c9c7f065faf66ea22cdbea16ea4674e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda74f47b7b9c90ce798edeada02675ef97e8ac74f1178cef5feac960180633`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9768de82b254bac1f6c596736a6c477a1b209c68a8daacb29881a7f543a19`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 121.0 KB (121025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3daf5722b2ebc36133727a34c50623d2cc4133160f21c65540805b5cc17c70`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 3.6 MB (3648319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9c09932e4005094da68ef3ce2c5dc4b0eb4417622e858e7cc7f23feb4e666`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518885ae4cee8048bd89d6fedaa71ba36e5ed6691b30739e46676fbe90b2e92d`  
		Last Modified: Tue, 02 Jul 2024 08:44:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:642fc7cd8e5f9acc8577a9ca5869bc2022717caa406906d839be82ac96a85dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1326313b20a01c486645847a0cefe6f9d247f946aa5b4933ca72b947d5725`

```dockerfile
```

-	Layers:
	-	`sha256:cdaeab0590b1316c34249297b1b53d0ab2a8bec7efb0c730416f27e0ac32b3da`  
		Last Modified: Tue, 02 Jul 2024 08:44:28 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae28ad90ea89b991e1f9ad04cbfacbc0f2401c53c1a22d9eb16e2640432eee`  
		Last Modified: Tue, 02 Jul 2024 08:44:27 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:99350c3328fe9ab8c2c62b304100817e06db1883743af824d5d790cfe4fce258
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
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
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
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9e0c77bc2592abf62bc2cf3ae42e9b922e966fd2d3f341b14e9daa16ae71f024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32336031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534df337ea9166611422a9e058d850623b1749c1a9846d287eb0b8b3e33053e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7909e1f7ac0d00445b2eddfec259336a5b57ef7d9c3c258968102dd19c6571`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c132c075bdb41a15e13ba12da7727043533dcd509f6b3c40ce0631ba78a3dfd5`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.9 MB (1937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afa6dbd1e2fd2ddc5c2c53d2dfe064505604c7bbb8752542ba7f6f05a95676`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.3 MB (1252996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71988b5aefe34ce51c5e853d041329cce96e191f83189af1078d89dff84c5c70`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23505095ad5510cf655e5a06b22abe66a69cb4b8ada3191ebed3ed083004eaf`  
		Last Modified: Fri, 14 Jun 2024 00:19:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1428f0f6cd3f8db559d5b911a5ce48a2cdcf086e3cd560fc466a1942596e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d207c0879b9e33e8884fd2ce7b6fccc9c2090971a1a5d1b425eaaa1f2d53`

```dockerfile
```

-	Layers:
	-	`sha256:0ef6853745dbda54a007383832c9eab98a44361f2001fc3b3a2f9f224e05a746`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4fcf7d4703e9804740cb368c205a56d353942a372564b34b85beb85afd430c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37164129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28a3f4cfda917b0c3a6e9eb919abb1a231e22e2411496f8091af07840b1e71f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855a9e32c179482484e2ef5ffc17445bb57ecdd08e7443eaf8cda621f379737`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb232fc864a5d885f4fb1b20ab634ec07471c1ca7d43ab5c6221ec79c03786`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.7 MB (2698425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcba21c1ceb62fdba693aaba8e20c36e599edaed883b605d8609ae5e33af31`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.3 MB (1322991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6a53eded239d055f27715b3b49d5d3a23a44a8b9597a2e05c9e0e22a83235`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530491c4ea43b457dd3b0ef88072d04ff9408648be3eec6a5ad89da9c2f23372`  
		Last Modified: Fri, 14 Jun 2024 00:50:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6a618ef6732e315dd52681d26e1fca1eb4a87b4786e29de103c0294d2cd77237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f114c22d73533b1f96b04ad77e637292c820f5805b01bd86a95d91086ed67`

```dockerfile
```

-	Layers:
	-	`sha256:65862383c3cf61bbe9427abe06e1d99e9a352aa8d3fab4a51596f03e311de608`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8483c5e4f7ee2946118c339543ebbaad7e1ef986db3e379b5989e22cea5b5070`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:99350c3328fe9ab8c2c62b304100817e06db1883743af824d5d790cfe4fce258
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
$ docker pull memcached@sha256:85fbae3a2eb651f6f9490684d8a84d56948280d5cc4128ec272e19f87f4a8c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02edcf1b9d09647586c521f2a44e0f9e7e33730212ea3ccd369dd7fd5bb4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bc51a7d5760b00a9753a8bcaa56d94cac429b7796f4621e2cf9581df638bc`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382790c27e5386ca4b9285691006bc82022cdee89619ae81ed68c6e91ac1721`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 2.5 MB (2489454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dfdf9a24fe886b4e44f9a244714e2f3398c01a02ff006e95b84968159aca7`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 1.3 MB (1253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6b75b31522d2441acd752e01a94a3d9f20034bf7adc51252e791da2f8dc3c`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176f2b53839a1f371083ccc27e20e98f2846e8729bae9e60f79a9ebfc109ab`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0d91b6ff5590fc618d9b0e82e771a61044d351502cdebb26db2b8021ccdb1c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a7838e5f4cea06ebce7d8df4412b2afdfd35135964ec1c3418aca318d3e882`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b6432ea0f4101a88bd00ae6ac2d1af1d87c8fb394a74fedfc710064ebb74c`  
		Last Modified: Tue, 02 Jul 2024 03:06:57 GMT  
		Size: 2.3 MB (2261289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb14fd923ec5ad414f0a88c9e1d3494a0286c2788b71eae99418548a1ffb2c2`  
		Last Modified: Tue, 02 Jul 2024 03:06:56 GMT  
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
$ docker pull memcached@sha256:d82717181b2e02ba383fa6d20b92231afdfde989f0f00b50c76fbe2d4cacf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c32dd60addd293dd7917bfd41b88e4bc52525e5abacda4e19f7deeb31abb1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e3f2985dfed6c28d8497e401d8b0d25617de154d5acf0d375fd0096c3bafb5`  
		Last Modified: Tue, 02 Jul 2024 03:07:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52845eb498a42472280eaeef57a28dabf9f9eb9adf93097bdcd55166fae3e815`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.5 MB (2495285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075cf82a5874faa62b87d0cfef6059cf5987e73fc8586bcae65f1747be5c009`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 1.3 MB (1254742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9590d95f70b5cedbfeaa65590d89a524030be38680638c56601a1604ba0362`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a4919a45f29427130fcad679ec2d22abd7936fdda03bb0e8f649113de2690`  
		Last Modified: Tue, 02 Jul 2024 03:07:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8fa762739db77aca985da55bcfcca855bef1b6fffc38fe81d99f558a9c1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0b3a401df3b0755f749cd34285180cc3d41a63dcf7e2009b04a73f9ee0aeac`

```dockerfile
```

-	Layers:
	-	`sha256:e0eae20be5b520edc16bd31ee7f08f0d48809374597fc305918d6caf43dd490f`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 2.3 MB (2258387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d1df5b67cc22a21c9cc08ba69cd633d5c21d2fcf6a577eff2c8de7a23d9b51`  
		Last Modified: Tue, 02 Jul 2024 03:07:24 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:9e0c77bc2592abf62bc2cf3ae42e9b922e966fd2d3f341b14e9daa16ae71f024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32336031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534df337ea9166611422a9e058d850623b1749c1a9846d287eb0b8b3e33053e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7909e1f7ac0d00445b2eddfec259336a5b57ef7d9c3c258968102dd19c6571`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c132c075bdb41a15e13ba12da7727043533dcd509f6b3c40ce0631ba78a3dfd5`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.9 MB (1937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afa6dbd1e2fd2ddc5c2c53d2dfe064505604c7bbb8752542ba7f6f05a95676`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 1.3 MB (1252996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71988b5aefe34ce51c5e853d041329cce96e191f83189af1078d89dff84c5c70`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23505095ad5510cf655e5a06b22abe66a69cb4b8ada3191ebed3ed083004eaf`  
		Last Modified: Fri, 14 Jun 2024 00:19:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1428f0f6cd3f8db559d5b911a5ce48a2cdcf086e3cd560fc466a1942596e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d207c0879b9e33e8884fd2ce7b6fccc9c2090971a1a5d1b425eaaa1f2d53`

```dockerfile
```

-	Layers:
	-	`sha256:0ef6853745dbda54a007383832c9eab98a44361f2001fc3b3a2f9f224e05a746`  
		Last Modified: Fri, 14 Jun 2024 00:19:56 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:4fcf7d4703e9804740cb368c205a56d353942a372564b34b85beb85afd430c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37164129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28a3f4cfda917b0c3a6e9eb919abb1a231e22e2411496f8091af07840b1e71f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855a9e32c179482484e2ef5ffc17445bb57ecdd08e7443eaf8cda621f379737`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb232fc864a5d885f4fb1b20ab634ec07471c1ca7d43ab5c6221ec79c03786`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.7 MB (2698425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcba21c1ceb62fdba693aaba8e20c36e599edaed883b605d8609ae5e33af31`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 1.3 MB (1322991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6a53eded239d055f27715b3b49d5d3a23a44a8b9597a2e05c9e0e22a83235`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530491c4ea43b457dd3b0ef88072d04ff9408648be3eec6a5ad89da9c2f23372`  
		Last Modified: Fri, 14 Jun 2024 00:50:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6a618ef6732e315dd52681d26e1fca1eb4a87b4786e29de103c0294d2cd77237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f114c22d73533b1f96b04ad77e637292c820f5805b01bd86a95d91086ed67`

```dockerfile
```

-	Layers:
	-	`sha256:65862383c3cf61bbe9427abe06e1d99e9a352aa8d3fab4a51596f03e311de608`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8483c5e4f7ee2946118c339543ebbaad7e1ef986db3e379b5989e22cea5b5070`  
		Last Modified: Fri, 14 Jun 2024 00:50:49 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:5940d9cb90ddbbe6a934bd7c06b1badd63e0139f6722ada202ac92776774ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c33e70c5e6dd0627e2f8f70899f73c8bd38a27b4df8b127e46f470223a7654`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029f5e40cd6de05b5805dc60b16a7d44d2e749279b0cc9c7907f297b544e06c`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec7095b95a5d047ca8c0c48a92aa739d81b97b535639dbd2f22b752031802`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.2 MB (2153919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48aa38726d0e9d9c83c6d83c486725aaeb031022d274217c287382a8077675`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 1.2 MB (1233318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1436daf4414b30a00187b4716f725eba3e9fb66f0356614ac4c83c757e56837`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c235abe57436f78aa1fd00eae85eebd7281b3bcec298bcd94d76ca533d1f7398`  
		Last Modified: Tue, 02 Jul 2024 06:18:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:256d9214020afa5608337fa25e737586616cde818ebce981618a03c4c6dde3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac6202d6904ce76983aab5ef2d0341b94b73437221be2f325881d252bcd38`

```dockerfile
```

-	Layers:
	-	`sha256:f97486ccfe602d50109ef83d537e9bf6171c6152a34e4e127519ca3e68afff0b`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 2.3 MB (2261110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1c3e9e2cdf043d6132efc54f683f57389d1d7ed66c08dd6d2f66ed1fcdbbfc`  
		Last Modified: Tue, 02 Jul 2024 06:18:09 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json
