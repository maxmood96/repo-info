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
$ docker pull memcached@sha256:978d23f130edfd5e165be7ccc968117d4f305c65979e0129b65c38256ebbf554
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
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
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
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:4fa9f7832517d9f4782d851fd21864a1ec95d7245abe27060bbe8661ad9e1997
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
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
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
$ docker pull memcached@sha256:978d23f130edfd5e165be7ccc968117d4f305c65979e0129b65c38256ebbf554
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
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
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
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:4fa9f7832517d9f4782d851fd21864a1ec95d7245abe27060bbe8661ad9e1997
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
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
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
$ docker pull memcached@sha256:e9fb414b17603319d3f00cd82094cba97c5933735b3fcd42e375ad0d4b606486
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.34-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.34-alpine3.21`

```console
$ docker pull memcached@sha256:e9fb414b17603319d3f00cd82094cba97c5933735b3fcd42e375ad0d4b606486
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.34-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.34-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.34-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
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
$ docker pull memcached@sha256:978d23f130edfd5e165be7ccc968117d4f305c65979e0129b65c38256ebbf554
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
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
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
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:4fa9f7832517d9f4782d851fd21864a1ec95d7245abe27060bbe8661ad9e1997
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
$ docker pull memcached@sha256:b2ab589832b48b83381cbd57821509a992538b42311925c72579ca38dfe5f80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebc545ade907aa85c39f9317596f1d892dfef6594086edb186fd946c385751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473451db0f7f9060bf913ec586773f3468ec50518848588f7c820fbf4df43764`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da232d2ec36e42bdabd55e130c8d6fba35bd3945d43c6a84457a88b60c29995`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 104.7 KB (104678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b974b3bc002f844cea917843ae7fed953430886460c99a652aaab555435a180`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 971.6 KB (971568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee89c7503d281db6d34633a28abbc8522aed61de8ac03dfae225f01e154ed8`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15426c94ef601def2eec902f8233d54689e4635bfd960a5f3e53aa93120c87b9`  
		Last Modified: Tue, 24 Dec 2024 21:35:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:08c1458e83a6bafeeec67c518f004f26375c8999365cea183ea85f4f580665f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd4112246fbf3f5c519829f38f426435c0f4cac2dec0d3821f519a37056628b`

```dockerfile
```

-	Layers:
	-	`sha256:7f5afcbcf5544a2190249dba6f0f41275627f28e701154d953ab0fd6b1ef5840`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bd64f6b6b72d8c91d59f5e89e01c2a667da3948c3157577c7abe3a8d5dc5f0`  
		Last Modified: Tue, 24 Dec 2024 21:35:42 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c596628ee3913e4289bad7bffe45e12b0a9df3bbcbbcdca323ad643acdab8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a686c9731e814cdbb4167f3d8f5479e973a34c51c39ea7974365506e39ab4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5840891c0f58a7c97179707a851437d1e9b7945c9fa5b89e5729484834c43a35`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5a271c958ff9f8f9f89bbaaffa3b17ecaeff0e5424515a244875e5172b4af`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 120.8 KB (120770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b4246b68f7e2246ec7cc2174a16f064dcabdaf440b1a6e79abf75dea61b94`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 970.7 KB (970695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d4032726313ae107ff50ac49d8be4d8aab6f6a93f83ccdd64c7f901f39f5e`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e0f1018a7774b391633bf7fceca8e20ed929ec3c3e3cc085c50b75e43dd56`  
		Last Modified: Tue, 24 Dec 2024 21:41:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e2366659524efd0703d7d94c23f6c3569787f26831997df30d5e775cd01920d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd98826d2f052e61092adf72fb77a809851bdef1954ff3c4c7dfbceee5a5e89`

```dockerfile
```

-	Layers:
	-	`sha256:4fca29daffd71b7874bd1f1db85f82ad46995cda0b4913b71105a9edbc30c890`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e383d40333d9193c997f72d01532a5ef04da9f73355e3755c740c5e95cf3f7`  
		Last Modified: Tue, 24 Dec 2024 21:41:10 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:ba86dc07a81498988b45ceb30a53ca9b086a79472824b59c46401f0338505b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d85cdda1e5277661fff21bd0dd6ad3d6c09798c9f0639bfebc835c2315cbc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40bccac59777071814a7c3bf48c92ab2b9b02a70db58227c273f56ea17990e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947791e35771d44b946632879ea90978a4dc43d772459ca9edf649f1a64ad2e`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4a0390b4f6b69c9576c9f5c74ba972995348ea6560f7e9c70c868afa8a436`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 963.6 KB (963617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d275998d4191bc0a5cedf749ca9deeff2ceface3ad90fa2d82c3596a4fcc0`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b415cb961d8cf571bafeacb69e80c667d8937215c11d38dd84ee19ad819f17f`  
		Last Modified: Tue, 24 Dec 2024 22:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:aa0b5509ca62ec478a184c22dd5441d552a73d7ac944afa954711e7083d6696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83614ed427cbccaad0fafaec5c93ac6a490c0b9b2d678e47f3fdb80d3f75a5a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3c424893ab49c829ce3fb8051e065b6647875262af93a10f3f76c84420630`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022cc5b0745a004ec031ea5a84b2e28bfa6749c5f1e01cefad7bf4196b87ccc`  
		Last Modified: Tue, 24 Dec 2024 22:34:01 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:a4a3317c489fce749470a72859fcdf1fe2d2266000dfd5e4bad77f16a07f611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4703827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0394c8268a5eb771c14037bf34890b78ffc4de6667a777db0ffe3f0886c48794`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.33
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Fri, 06 Dec 2024 01:54:11 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Fri, 06 Dec 2024 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Dec 2024 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 01:54:11 GMT
USER memcache
# Fri, 06 Dec 2024 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Dec 2024 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1bcab4824c6a8e7a4114ba48dcb356613c881fcd975ae057090e80ab9f13bd`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff721cf8c91f5a1cc75114b754ead14a9c513e6e406022bfeda8bbbf371aa73e`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 124.3 KB (124266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fea0cc369b407b555b9d475ce0e1123cd6f9dff74df74fd5b02a5ae0edbe11`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 1.0 MB (1001088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22004fb13d9893326267cd5f5afd69aabc63a4f9ff1449364e70c10e2ec7d19c`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b537353239642c336d219806ce7f9749300bc02e86f555ee374d5f650a7878c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ae040b0c2295d2b423db19b4db3fa77b653644e6239d02add82283c284c8f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 KB (111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c5cc63b271298a1f669d43bdd64b47017e313e0cf4f15e271da10ad26f22e`

```dockerfile
```

-	Layers:
	-	`sha256:ea73581dcd5dba8f843e4e04a9916b4ad91db0e4dc0ce1ae3ad68e22e6590535`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 91.8 KB (91828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220354003bffb339d8943f93499e56ebd89109d53e7cd46b509916a4d07ede61`  
		Last Modified: Mon, 09 Dec 2024 20:32:02 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:5f054d37c1e5885770f8f0934adb1dc98f95b7fee05faf0647143f37a2941abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada50f49b5e1e4a37ba0f61c79acef330af7d48678cc063b9836f53f282d660e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ae3782f03e34b7f962101d492667052a66543aa8f23bff983a9bc60edc9a0`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91987269b07c9becfcc1841a6b04df3d9a01709b8bc7e4552dde1a3c5930711`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 113.4 KB (113439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c24936ea0d3fe427e471b452767c718210913209dbc03f30c00e503db1f9471`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 992.1 KB (992092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687118fab3fd4c181ff4725baa3df4f1ab5ef62d5f86d048209984deb268355c`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a0e96ada6db9df21aae8d06e736d457377e74e35d27b3ad7bbcb1702ac1692`  
		Last Modified: Tue, 24 Dec 2024 21:42:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:55b28c86428ceee68ed6f4179c3cb9fa528b0baf46555e493531f3dc09d25d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc375450431011c02c98aae3d8121efd62b26f2e49413f27b7a734cda996ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:07d145a04fbc7cd73a94e45ecf992c02bc7a4adeec5f99f4baa382fdc6eec10e`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41807b5525ef153504c26baa0242445a7415a422bd289d07a1f345d2aa4254`  
		Last Modified: Tue, 24 Dec 2024 21:42:57 GMT  
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
