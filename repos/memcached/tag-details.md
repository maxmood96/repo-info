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
-	[`memcached:1.6.26`](#memcached1626)
-	[`memcached:1.6.26-alpine`](#memcached1626-alpine)
-	[`memcached:1.6.26-alpine3.19`](#memcached1626-alpine319)
-	[`memcached:1.6.26-bookworm`](#memcached1626-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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

### `memcached:1.6.26` - linux; amd64

```console
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26-alpine`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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

### `memcached:1.6.26-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26-alpine3.19`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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

### `memcached:1.6.26-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26-bookworm`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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

### `memcached:1.6.26-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:8906e7654a202d07e6b1bd6a1382b309e718feb9084987c365337ec8161ccaab
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:f71187b8c3d99377ce7d267fff16218fb004a1b542236d414c67820364c37e89
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
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json
