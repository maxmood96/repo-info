<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.21`](#memcached1-alpine321)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.21`](#memcached16-alpine321)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.34`](#memcached1634)
-	[`memcached:1.6.34-alpine`](#memcached1634-alpine)
-	[`memcached:1.6.34-alpine3.21`](#memcached1634-alpine321)
-	[`memcached:1.6.34-bookworm`](#memcached1634-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.21`](#memcachedalpine321)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:3e528363baabe61307eaccb3d65e11be4ca44492fa21b31bebe06e8c6c2bd8b6
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
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:375bc4a61dc65edd8163c937d69501c0325b5c7d7660f6974982e2d1a309997d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e392ea20bd35f4d756e6ad6715b6f827c20e0123a8ad74bac56b2122e42b76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.32
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.32.tar.gz
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a6377de830d15e17b769184df6ad20766c2279d9
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
USER memcache
# Mon, 21 Oct 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 21 Oct 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 18 Nov 2024 05:57:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73411748d41c8900a2e46b2e84cda57890db94ff010e5767e7d503fb301c5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434574b080a33771844da9fe1f65ae99a8060f103229f83485f9b276ccbf830b`

```dockerfile
```

-	Layers:
	-	`sha256:1282c9de70eafb095b4d790a1e60386966df96e786c3e1acb71c18a762e42b04`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:03cea0adcd7595491cba44399087f6f401c8c94ae884c6f1d5f00f04a9f7f31e
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

### `memcached:1-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:3e528363baabe61307eaccb3d65e11be4ca44492fa21b31bebe06e8c6c2bd8b6
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
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:375bc4a61dc65edd8163c937d69501c0325b5c7d7660f6974982e2d1a309997d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e392ea20bd35f4d756e6ad6715b6f827c20e0123a8ad74bac56b2122e42b76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.32
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.32.tar.gz
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a6377de830d15e17b769184df6ad20766c2279d9
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
USER memcache
# Mon, 21 Oct 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 21 Oct 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 18 Nov 2024 05:57:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73411748d41c8900a2e46b2e84cda57890db94ff010e5767e7d503fb301c5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434574b080a33771844da9fe1f65ae99a8060f103229f83485f9b276ccbf830b`

```dockerfile
```

-	Layers:
	-	`sha256:1282c9de70eafb095b4d790a1e60386966df96e786c3e1acb71c18a762e42b04`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:03cea0adcd7595491cba44399087f6f401c8c94ae884c6f1d5f00f04a9f7f31e
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

### `memcached:1.6-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.34`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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

### `memcached:1.6.34` - linux; amd64

```console
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.34-alpine`

```console
$ docker pull memcached@sha256:03cea0adcd7595491cba44399087f6f401c8c94ae884c6f1d5f00f04a9f7f31e
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

### `memcached:1.6.34-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.34-alpine3.21`

```console
$ docker pull memcached@sha256:03cea0adcd7595491cba44399087f6f401c8c94ae884c6f1d5f00f04a9f7f31e
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

### `memcached:1.6.34-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.34-bookworm`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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

### `memcached:1.6.34-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:3e528363baabe61307eaccb3d65e11be4ca44492fa21b31bebe06e8c6c2bd8b6
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
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:375bc4a61dc65edd8163c937d69501c0325b5c7d7660f6974982e2d1a309997d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e392ea20bd35f4d756e6ad6715b6f827c20e0123a8ad74bac56b2122e42b76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.32
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.32.tar.gz
# Mon, 21 Oct 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a6377de830d15e17b769184df6ad20766c2279d9
# Mon, 21 Oct 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 21 Oct 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 00:54:11 GMT
USER memcache
# Mon, 21 Oct 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 21 Oct 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 18 Nov 2024 05:57:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:73411748d41c8900a2e46b2e84cda57890db94ff010e5767e7d503fb301c5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434574b080a33771844da9fe1f65ae99a8060f103229f83485f9b276ccbf830b`

```dockerfile
```

-	Layers:
	-	`sha256:1282c9de70eafb095b4d790a1e60386966df96e786c3e1acb71c18a762e42b04`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Mon, 18 Nov 2024 05:57:30 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:03cea0adcd7595491cba44399087f6f401c8c94ae884c6f1d5f00f04a9f7f31e
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

### `memcached:alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:de65617c7bf16c4de35efcbd0340c268f48bab274dea26f003f97ee6542fc483
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
$ docker pull memcached@sha256:97fe2f687ff80e7daab7909d963b6b8fad595b59a6c7d378dc368f3300aefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d21d94223c4c4779858d71906e10216957f8b49f810dc54793710d708118d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379245d17bd5470125a361e3962e3c1bd718b5ab33dc724938d91db5f986622c`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf73dab96155da1c01ca6f92cc50ea4eaa766cdc08df0d4864a5d820492f87d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.5 MB (2491753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3e0ff325d3c655cce174fe14df9c9cff1aa9946a3a1b8f4687148a607306`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 1.3 MB (1267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856f7076ffb80e9f7523eb06e203a5b3bc3e4d1727ac4ddb7c028cc020d3d2d`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8c9fc1c0023bdc9e9d3fced306697e617073042631f5fac9bf0c9a5857aec`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:fc0c7eb92cf8f4941de6c7c0ae90c1fa87604255262516466a2a93e1e330888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d57952316b99ceba063a947c6af9f45484c78d36c1acd7cf0189362f73a05c4`

```dockerfile
```

-	Layers:
	-	`sha256:0dd3c14fd0aa26441ef7fe13481cba4e038306ba231372987c9dfd294a0c3c2b`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d869db1d32fa93d55f2622d830b75f15827d12d439a332039955e1a052bb3`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:81d677cff9298cde40d5f21da0e63749271d22cb3ef67b950af4c581c42a20ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29098800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc0b855dc054aa34aefa5178f9ed50747fa1f3a97937ba622fd4a7fdb65c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14209fabe4a80eb9b178ecfe79d1bb105587036b015407306770882c8d14af`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc82217958354f4a330c00f3256c98d31c28238b1a8ef9f46b9ebe6b06a4f4`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.1 MB (2096088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7c177fa36879b5b0cb63d05330fc53775ddddf42cc06f954ecd529b351e7`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 1.2 MB (1246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28db8a1c43cc64546c35b0a17509e5c6e3f4594adb0590d9d83c3fd2ecc897`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedc027585cd440b347aa80a770d2c4ac16b9731d3a9538431fc10da48a38f`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f928aa4b4896a9f0ca46543906cf4982d80c56d750fca64679f78ea4f965f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adc41e1391ce812741c2729a8817ea7f2c3ccdee019560320898f087f2252`

```dockerfile
```

-	Layers:
	-	`sha256:21b5a23dd50198212df757f1de7da29a05a695e268e806667c2284b999087eeb`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01aa77ea9cfb3955a5dcd519dd08b14eff4f7e53757b61293d8ddb97535f269`  
		Last Modified: Tue, 24 Dec 2024 22:36:59 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:068758c1c8a41bb4c5b93daef3675109597ced52abdc7dacb81edde553caa12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31676562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec8fd9f7cc5ca8632235376f81b1ee9cc60bb09daf12a533e7a3e6cff70a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cc3ca0cca60072c459d274c524b7df2d2cfd91422734ddfca8681d445b74e`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cc9fccfbeb557a0fb8bf1b82f293cd18703bd3d0830092d10ffb46faf6ec9`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046431d0aba356733aa2a86555a9b4e7814c979444192de7db0debf5c723f092`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 1.3 MB (1261023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcdd0173852319bdd08909c22ecb62d3c2e2283992a3f916c41ce743534162`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d3424e7dc9782243613e405c428d8eaba3c3c1afc5e0b4b0ab9735f1f387`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f17ebace3b77ba3b5fcf8383d36b5e09455dcef0707e9833a3a7bc2119300193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ead862064dbb5331ab45f03b8656e264d9adb621bb971e4c4b520a3724eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:db24f4528be744988c63fca31222013180bcdadb86334c248e291cc9ba033025`  
		Last Modified: Tue, 24 Dec 2024 23:02:16 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5ad8e5e127b3e6b9340edf2703ccdbb69a7403e2c0d1fddc6010eee9aaab7a`  
		Last Modified: Tue, 24 Dec 2024 23:02:15 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:7304c7658167299afd98e177413fb614ef59fe42a181fb9af6446fb04ad556cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32974087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3f1a2308f2f5792ae7686204e1d387f57ff6d025dfa788ba287c46e1c72b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668afa22b9bf58fdc652c0bffa14ab0b18a0e4fd8af05544403efd3ad6a7746`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44ce24e3068eef0e86047ac448ce589cced4bacc43c20d5e24653c921e8a91`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.5 MB (2500692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cac25950ac95698a0165bd9d76cd431b3b55f9c94f8b751d71f524368ef277`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 1.3 MB (1266496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3a9816675aa6bc561b7a58b7b756c94a09951adbc1b2f692b831b73b4ad4`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5647099be9e38a3ea1440a1e179dd4f3e6957ed358de0a84ebddaafdfa69526`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:857ed13ba51e07c0104c0f5ce92121ca5ba1398b5d081e6a2ae8225decee7207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb611c1b69d4057cac1fa46146bd202e944e34197d19daed7088372c4381f7c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2294215ca6f2b1523215e5fa1ce1e3b5473d4edd173240b9cb19400674cb1f`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8517c53ea77f967a8fff21bc6aeca6df5012887055182a0dfdbd36e6ea6c5b2a`  
		Last Modified: Tue, 24 Dec 2024 22:17:21 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:115cd3f0d283e6284637dba9ad70b55bc91d39623f880252e98118f95574380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdcb0db9d957f24be9a783292d0b8451cd10c25b81cf6fb309d7f042623705b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02202985a9e09dfe1ef64f96d7f2e5b83d3f3387954475784f9c17c2715166`  
		Last Modified: Tue, 24 Dec 2024 23:19:04 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e108ba613205d57fe4ea372cda7204672f2df99cd34132d95cf9671bc99386`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.9 MB (1943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6a5a374f2ba0688a66eb4354975936391da130955fa8ee929c686b5249d5d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 1.3 MB (1261937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b6b8ab502693a2ca11a8b01ad50f5ad0e90f5a28e3a290e75d3dc43d93299d`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5007207cf3ab9c432c483567ea2fa81e6cd1e061d43eb8c7d505fac415aaa`  
		Last Modified: Tue, 24 Dec 2024 23:19:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:41f9ca457ed93c3ba41ab42008a89cb09451e7197d195bd65212bd73755803d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc327d222790f064993d78f8fa832d2c76621a9e209353e9eb799130825b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7717e0cac9208a05fcafca2ecd7c721a1b5dceb9a04d72de7fc2f16cbee87be6`  
		Last Modified: Tue, 24 Dec 2024 23:19:05 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:cc2249f32fab55b9cb94b1190495f7a7e8d51a1590c58c333bc9f1b1d4f400fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36104986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cec3f747f512f5cadab6d83fda7440ba88233727e63221cef096d8be2c2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cbf88bb15aedb586605ccad1dc38f1331d5d56d774825d5e695ff3bb6bdef`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bba66c678c571042567045c499de22980823c2d424e4aa9220aadf79264e0`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.7 MB (2708552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6a1d8b446b311a32c3f553a64556f921b822ed8a0d2ad929ed64aa65a9c66`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 1.3 MB (1331686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeff7f0be621827fa53fbed3be8d2172bd7d1bd711dbb5b20464e9873b0dd45`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a694a42426b0d01abd0b946abd403bd5a1a2e7eecad1b51c4d1a7394993f8d`  
		Last Modified: Wed, 25 Dec 2024 04:17:28 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2675930f2f0e53fd5476c893f872aa97701aa788a19028e0c239abc1ab100338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b0c8f7f7a5787591ecbda1521d32c13f4cffb2ca1b0c02a2c353b3731889`

```dockerfile
```

-	Layers:
	-	`sha256:7627f9bba51e6806d26c1f156a4ab61d6bc3e58b479538df9de0cc0258b57028`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e217ed2fc84ecf9649805254f1f73a9ff9ba29895d4bf17f952e918940f3a14e`  
		Last Modified: Wed, 25 Dec 2024 04:17:27 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:c8c357e12080b73e6cafa27cca6a1bf70543907d83c185eda36b30a1d6828bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30282580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1c4998b2073d7cedef4f5085eda485dacce53d48c4ddee2e2d12488c3bb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f39a5bea4c27739e800eb83122e53124bb03988d1662b2055a325e93059d5`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ad3f1eb73fe1651c9ee7714e25023471b1f8bcfefad492f60fedf88878c76`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 2.2 MB (2156377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482561892bc147abcd8c74af5691a7f8b1bae84cf7119b7270be2743f20ecc6`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 1.2 MB (1245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bb3ee6ab17037d069d7f4fc9e4f17c9865b03ea5f1c8db8c9f9d0c56d1bc`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9318b45b226b1521053a0c1ca55ddd1fccbd1f40c3efa3abe1ab72ef51fe3`  
		Last Modified: Tue, 24 Dec 2024 22:36:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:be9ce53aeafcf7b1f123e8b46a51c1dadf522f5c288d94ccfb98ac02482199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272ad1f0978e6c76c3977bba1f54cf4055d41f7c162bc820e3aa8b3f9531ddb`

```dockerfile
```

-	Layers:
	-	`sha256:210566762c119a05ca5e99924d8738143139a925a1bb6ffb90d9a0a9bfd48aee`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacc5a59bcc440088269478012e23b6f27c44b7461b3d1217b2849f389938af`  
		Last Modified: Tue, 24 Dec 2024 22:36:31 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
