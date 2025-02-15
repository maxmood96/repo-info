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
-	[`memcached:1.6.36`](#memcached1636)
-	[`memcached:1.6.36-alpine`](#memcached1636-alpine)
-	[`memcached:1.6.36-alpine3.21`](#memcached1636-alpine321)
-	[`memcached:1.6.36-bookworm`](#memcached1636-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.21`](#memcachedalpine321)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:f0f3c2a07b8f5d6ffe7bebab5bd4956166b919ce83a56958a641fe2c2d5b2aa9
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
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
		Last Modified: Fri, 13 Dec 2024 16:51:49 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 16 Dec 2024 10:11:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Sun, 15 Dec 2024 20:07:21 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Sun, 15 Dec 2024 20:07:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 16 Dec 2024 08:39:05 GMT  
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
		Last Modified: Mon, 16 Dec 2024 10:11:31 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:18a5543b40a3187a5bdfdfec62a4900b010267288b4a059c6dbbe75504010d8f
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:f0f3c2a07b8f5d6ffe7bebab5bd4956166b919ce83a56958a641fe2c2d5b2aa9
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
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
		Last Modified: Fri, 13 Dec 2024 16:51:49 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 16 Dec 2024 10:11:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Sun, 15 Dec 2024 20:07:21 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Sun, 15 Dec 2024 20:07:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 16 Dec 2024 08:39:05 GMT  
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
		Last Modified: Mon, 16 Dec 2024 10:11:31 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:18a5543b40a3187a5bdfdfec62a4900b010267288b4a059c6dbbe75504010d8f
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.36`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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

### `memcached:1.6.36` - linux; amd64

```console
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.36-alpine`

```console
$ docker pull memcached@sha256:18a5543b40a3187a5bdfdfec62a4900b010267288b4a059c6dbbe75504010d8f
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

### `memcached:1.6.36-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.36-alpine3.21`

```console
$ docker pull memcached@sha256:18a5543b40a3187a5bdfdfec62a4900b010267288b4a059c6dbbe75504010d8f
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

### `memcached:1.6.36-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.36-bookworm`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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

### `memcached:1.6.36-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.36-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.36-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:f0f3c2a07b8f5d6ffe7bebab5bd4956166b919ce83a56958a641fe2c2d5b2aa9
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
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
		Last Modified: Fri, 13 Dec 2024 16:51:49 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6786e45e7400ad792d8dc25dbf9193de1e8860629a6a2e795b45e1cd75dee59`  
		Last Modified: Mon, 16 Dec 2024 10:11:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5199b90787ef0f87957108a2e237056abc9b5dbab8a04b742b6d0353d88cb785`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 108.6 KB (108593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f6800f6b6e4d4f4aa5884fd49f66ce3d94275641e62963f1685b916123058`  
		Last Modified: Sun, 15 Dec 2024 20:07:21 GMT  
		Size: 2.9 MB (2906396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823139de9224f2db03fbfa7db151caa25689d1cbe251c294e38db726b959ea89`  
		Last Modified: Sun, 15 Dec 2024 20:07:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170039abf6abfcdd0cebb4d3a758124d6d6423f3af956cae7bf6d7e4246505b`  
		Last Modified: Mon, 16 Dec 2024 08:39:05 GMT  
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
		Last Modified: Mon, 16 Dec 2024 10:11:31 GMT  
		Size: 86.1 KB (86097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24139c1500f979fd0872b553f4fc36736a7c840e494192f67e711feeab445dcf`  
		Last Modified: Sun, 15 Dec 2024 20:07:19 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:18a5543b40a3187a5bdfdfec62a4900b010267288b4a059c6dbbe75504010d8f
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
$ docker pull memcached@sha256:ceb4980dead474762bd92403f6a06afe99d37e4b49d03524dba95cae1c127269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0837de9fd756379ab48f6361f72e172b062a84a2459aaecf5b199717526b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31783bf88585c02ee723cfa158c9b8f0ef2f68d5e33c7ef771ab1f27da7d00b`  
		Last Modified: Fri, 14 Feb 2025 22:34:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfaa864e0a13ed279b0cd351ec17bdcda32231f2a08d9092e03cc1d5267996`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf91bccf03c52065a1c796c5a80c9b758fac48d2d1c2f654867131c3eea3aab`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 968.6 KB (968584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b31b4a4b14a6112b89363f7133901f51c8143dea5fa1414ab2ee15047958e`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b68a77ac568cc540377cb8f29e7df541cd95c4cb46d4e1f50d4f6198df7047`  
		Last Modified: Fri, 14 Feb 2025 22:34:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec2280bdd3974f892156dbe13e32755bf2bc247712b9180c1a122668c93b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5e720c1c54c2f212ca80a87eae56a4310c703450f06b442890bc8ccca12f4`

```dockerfile
```

-	Layers:
	-	`sha256:8a87c5b3d3bc3ef8d123a4bae3ba0f58339e5d8cd16558ecf4f033fcfcf0fbc0`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c7d574262bdfa92482c62c79a216a6c8c61dbfadd00e705052c88ec2aa4e2`  
		Last Modified: Fri, 14 Feb 2025 22:34:30 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7ec441942160a334458b9384e50e385658a251ddc6e149423adb3a4894cd83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866bb85950380f6e5d8ed5d6703ee7490056e87e4d591190da1e49aa0b2055f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f94861e5773df86df24a9099ecd3b028619dc17ff26f44ff4968096836bae6`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d47f9e36d59793daf5d888137b8e4029088eb5f20c0dfa050f0d4dea8a2d16`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 120.8 KB (120779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa131940c7243a9f000b89f7b1066f34f3dd666839d64e191ea12f6b77d419`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 968.3 KB (968295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b1beab15d2e99383134bff8269e9e7caabce12fc741a2ca99250a201002e8`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8205b3e9687b0f061ba866e9d7931a12494a7338a3ead62a3243177f8c73c`  
		Last Modified: Wed, 05 Feb 2025 22:35:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:c5027d555c2e29e7e7f92db7c094e65d60ebe7624b7a47e4f9e07e6bea36d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca8519f69b6375d02c2f42cc88bb32b5840c61879f4e4746498a5504eff4933`

```dockerfile
```

-	Layers:
	-	`sha256:f5c88f287b161deff38e8be49027540fd6a18807e5c135c35247f957050320f4`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d9c466f3c7ceffcb6cdec4e69f73403f6b4c96b0412d4ca7825524d07b7f8f`  
		Last Modified: Wed, 05 Feb 2025 23:16:30 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:c79f77b80eea8c79a2782c7643f2d927cb1bfb53ab97eef8d9ad4bf6617b774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e8926e25a7d57e7723eb0c21988e4dc7181be3d497623cc81dd9e08d395b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f314676555157be65cc23fa0bfd953b88c667def3348ff2a21b8bf81a2292`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856486aefa8f3f3d24a3e898964a12ac3276ad52888a1da9654f02b25504e87`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 109.5 KB (109483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbe48394f064e4abcccbe8180103a5232e0e1398a375d33865c084ad30c624`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 960.2 KB (960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22077c32293253677fe31d3448f37512e7d9e9b79874c2c6e37fe3c0482151`  
		Last Modified: Fri, 14 Feb 2025 23:13:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39f88512dbd7c3b2369145e298a4b6081ff14faa6d0a332c184f8514aca8da`  
		Last Modified: Fri, 14 Feb 2025 23:13:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9cb75e756e619bcf72577805c6d91447a8aa07d93f57975d74cfa7b06e2eab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a4b0790923cf8bd4efeaebe592147bd08898d6156deb16b07f425861973d3c`

```dockerfile
```

-	Layers:
	-	`sha256:097c3464950f4c9e9e5f12cbde8289de81675598e58f5dfe96ffd7df58eda281`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99a18ac26c0a34351290a8152451974a74858fe497ef893c060beb18d07a87`  
		Last Modified: Fri, 14 Feb 2025 22:34:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:c129ff0e031440f9324afbd328a999090d13feecd33d4bd5f28e4b36dcae03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802215733c7ef24ce06bbde44e7f7ea36eb5f4c1d5255abf6725638dfa615f23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d754b86e90887aba15e3cc20babe6eb7f675d64dbd65541a64331671a21f2`  
		Last Modified: Fri, 14 Feb 2025 23:13:47 GMT  
		Size: 1.0 MB (1006829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff11aca9aa85d0dade4ef904a85a7cb7daf4f3dfb386c434d98c4e5b82f7b1e`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0615eba7a56f1e0fd0dd6cc272ebf49f7cd6a2f113371a1c6b6968405bd058a`  
		Last Modified: Fri, 14 Feb 2025 23:13:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:95dc66f7ef612918c14ffde68b4e1e3fde823e6dce3663fd404f2186daba1bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629edb64d899e00dd1349e8a665231e5faa4b2008ad6b61939ad32cbd7dbb1f`

```dockerfile
```

-	Layers:
	-	`sha256:57e25d9d26a61bd1bd223ece4852767532e36ad23c2b1a255d8d1f1367dda488`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946266fec90856f30a2df7899c423ac83449b6d3f4116f996c19467a3092314`  
		Last Modified: Fri, 14 Feb 2025 22:34:34 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:b2563e592d6a06ef1b644f607a2ac949bf6559298e76c48046e545949c43fd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b85a22de09762e752f70897cc41ad2b7d44db906d599346f3225ba27862287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Sat, 15 Feb 2025 00:01:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Sat, 15 Feb 2025 00:01:51 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc0e2d6d114133081003f9baa195306a6678bebf0511034fea684cb326b6ef`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 988.6 KB (988641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87258bbf68d06618f4559ad9f49de93a6182de80f2ef82c0bb38bfd3cbd81731`  
		Last Modified: Sat, 15 Feb 2025 00:01:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5001411d9d4e67c9ef395174fc887f081fb2fb6a69f6b42d8624cc5398b70`  
		Last Modified: Sat, 15 Feb 2025 00:02:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fe460c3d974043b59e09e6d819a8aa2dcf48b85095a601cb2d727ae1c220cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecdc5730a0363cf7c93a541176f26b019a7b6acacf446b8cb4607fa89f4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:768e08f256174f99868001a2b49221566e7ef42b94bacbfc7b3ace11442e3764`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b26916c80c718a77c5f68b1f7721af52aec3458eeb49ce96bf5bc6e26a0eea`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:a1d3a1c601732fc04245de562a3667db0bc3ae6964f0e830183d4dd5514b1b38
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
$ docker pull memcached@sha256:f6fcc37965fc5e9bceb36faf9a79ac813bdaa0d1531b62d5da6cf8e99de2816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b59c15aa68629fa32650198907a63511120ba2da23c906972b085aff44d701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe6a863859e52ca9505c02913c1107b6228fc66cafce28b31f28f1937e0eeb8`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a6f44ad084592533f61486bf49fbab1fc98804dedd0f82a84219a1ec9daf9`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 2.5 MB (2491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b921a127d93d9135bcb435f07e48d1db90d2f956f4b0306813e5f2223100be`  
		Last Modified: Wed, 05 Feb 2025 22:35:08 GMT  
		Size: 1.3 MB (1267092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a5f3ea6b64738aa4a613a340d5508379d7b605e4d74b820f93ea9a19928e2`  
		Last Modified: Wed, 05 Feb 2025 21:07:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e1f8f474a071ea5b09e345d8b2bd48ed8d88f42936c8d130fbbcad11f4074`  
		Last Modified: Wed, 05 Feb 2025 22:35:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:37d76d8b84486ee869258ef61a1883a833ef732f27e4dbd43b82968970fa99ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f06e90614de31cd7771ecb5adb9eacb18db1560baa1268b80812a42f2a5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a9933b74494765fc3743423771e2463cf3869a4ae61a67cd9ab3725ff0b8ecd`  
		Last Modified: Wed, 05 Feb 2025 23:01:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacd9b9c6679c1dd8906bf1a6ebc726e7f59dc4e4f11cc64ad9ad8480a693a3c`  
		Last Modified: Wed, 05 Feb 2025 23:01:50 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1b9cd2bd6f56e7bdf3d5f1f1ef8705f343f4174cd1a442d220ed91b8aab6dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0219b2f23f7308f4ba778c17ac8a5d0d6485ba4499fed5955c91da72741805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Wed, 05 Feb 2025 12:04:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Wed, 05 Feb 2025 01:08:03 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f712b6f920438e107eb62f44b8e94f074a565884e50f5a031b0a443788b27e`  
		Last Modified: Wed, 05 Feb 2025 23:01:55 GMT  
		Size: 1.2 MB (1245221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da0fbdca4e6251e5a0cf218346faf0927be440084a0d930466554f32d2e838`  
		Last Modified: Wed, 05 Feb 2025 23:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7de694afdad6061a08611d3cc2c067a0b7ed6d7e414b9949fa46fc9416a038d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d815e28081315f0ef02dc6a366fc93c789ad9a92ddde251d20fdea04302083`

```dockerfile
```

-	Layers:
	-	`sha256:6900ca04748e1eaaf359a0a3844f78cf4942a6db4403689b3f1b9fda9b30d2b4`  
		Last Modified: Wed, 05 Feb 2025 23:02:05 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6beffa868494f73c99783e2587e3a754715bc8920ea4aaa5f6594ea9c442db0`  
		Last Modified: Wed, 05 Feb 2025 23:02:06 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1ef0cde695d1214d4d5c24be2fc2d38eff5c34ee1b88324b076bbe544683df86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9d566bd591423afa2315d04eb6b87ce74211b9d1770c9794f0572062b5398f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 22:14:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45a7103e9369684b5161d6e08f39a553ee8f827d418a789ee032fe2a371f94`  
		Last Modified: Wed, 05 Feb 2025 22:14:43 GMT  
		Size: 1.3 MB (1260582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff205ca4fd74a7d15062dd881973ff0d8f6789e035a0911d80c6c94085618c36`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bfc8ed54d556be877f6e457dbf8a27bcd2f3bb5aff921916439fde2f39d5e`  
		Last Modified: Wed, 05 Feb 2025 22:14:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fdee9b8d8020e6950be5f2b612c1016c35d76c7fa6a0e70ec0249cc9b8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820790c3dc8d773966628d49f14303d9fddbda622b6d57f167904d3ea28d0bc`

```dockerfile
```

-	Layers:
	-	`sha256:25f4e291a3d334bcb77f9b8f3df2fef977755cb03554d3e6eeb11fc84e7c9a7b`  
		Last Modified: Wed, 05 Feb 2025 23:02:33 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb133edf0d1fcc1456869ac6fc85b82e72bb26fd92678abab0218610aad43ba`  
		Last Modified: Wed, 05 Feb 2025 23:02:35 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:9151bba444d569256ccc0a6ff65d9c5b8f276825235afe86618114ba2f31b9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62003a6a166423ee9ce494ed4e08eeb9981abc09e8b2e21a1de17dfb722562f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cde214d5abc67057e7df470eda15c4af2c1879550278a660ded022e15445cf`  
		Last Modified: Wed, 05 Feb 2025 23:02:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc31c564e5c95f3a8deda2d815cc728c8e7f15aa8f770fe49bdf1127a2f7d8f`  
		Last Modified: Wed, 05 Feb 2025 23:02:41 GMT  
		Size: 2.5 MB (2500676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f10ab5f69c331a5ee59399b2d7b914f8684a44f5c7434ccda2cec85a9309c`  
		Last Modified: Wed, 05 Feb 2025 23:02:42 GMT  
		Size: 1.3 MB (1266292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5ee65fe5f3d89cf3d6597f7a525af8b18d46e350c6e54ae84f1cfb3c53b3e`  
		Last Modified: Wed, 05 Feb 2025 21:07:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8a06192a055fbd4471822f5efd2fc4f14faa90a1b81a62466fc93ee18f436`  
		Last Modified: Wed, 05 Feb 2025 23:02:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ff79b240a5ac0222409c4b6de5630441d966fb19be9e1fe4960f196a684c9252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228cb23582a9f77b592c24914ec1130fc918285faed6026841c7956c59348ede`

```dockerfile
```

-	Layers:
	-	`sha256:2a1fd9e48016e7d03061f3de58db17fed9d03f1aef46f35fd03481e1fa135972`  
		Last Modified: Wed, 05 Feb 2025 23:02:51 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8f57b5cd82a7fb9584a50e2664626a8c44dd503378d2218ab6a67d535ae3d0`  
		Last Modified: Wed, 05 Feb 2025 23:02:53 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:9d13ea63f0a66a41b7652aff28bfc87302304c754481f7febd754859885f686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4f4bfeffac275dc7c9df91c5428e6cd4e7db46fd700adbba9fb34eba55ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Wed, 05 Feb 2025 04:13:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 08:03:37 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d6ce9db92583af8676c477ca4fb3a2193aa12b09893acaaf268e9ef811c5f`  
		Last Modified: Wed, 05 Feb 2025 23:02:58 GMT  
		Size: 1.3 MB (1260897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d9887895f04fd853da4b6b45235672e323bbc1a545c162631fc4fdc22d1af`  
		Last Modified: Wed, 05 Feb 2025 23:03:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13aaaf1a662b43cb102291f1db3c30b074216b6fb232e07a17a9b4b482e9794`  
		Last Modified: Wed, 05 Feb 2025 23:03:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bb84ef63540a051cc568c963b17ba20edcd2b3d6af2414025481f5527cf49cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504278c88a7cdb1a0ddbf1c5e9a712aac245022400eed2aac68d0c6718b73ea7`

```dockerfile
```

-	Layers:
	-	`sha256:223cef58375e13e71a1a5ec8ca804798633fa347555be8fd441b94beecf6c098`  
		Last Modified: Wed, 05 Feb 2025 23:03:06 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:654b1fa81e7e0b1e312d10db2a179daef4b1cfb423b841f7b98096a2d5ba4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb02b77f4d421fb4a5c3efec863d7c8f26b5469c704a1fa3292e23a7fc9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 23:03:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 23:03:13 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375c07e0aeb2a5e5fca9c9b1d090ed708eac9cdf6fca904ec90c7c407cdb16fe`  
		Last Modified: Wed, 05 Feb 2025 23:03:16 GMT  
		Size: 1.3 MB (1330931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30f7e2c18eee863e59817f26bc13bf11bb51d1a7541a544a47749a86adc6ef`  
		Last Modified: Wed, 05 Feb 2025 23:03:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c45f5c9ba8b1deae9b934526a13bfbf7cedafa8039c2215cc62f381dbb48`  
		Last Modified: Wed, 05 Feb 2025 23:01:58 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a45f15e9227a42415b9b23c51849cc4385ee70c660c66d88f9764225f1f58d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeec6bfb854a8e0e7c66c4e56b5ec4e7526ca70c5754ad0d7ef793575f7d462`

```dockerfile
```

-	Layers:
	-	`sha256:466c057cd3e3e1d894ddc4eae72153e3faaee46339d3ce9f8e401c64caf26413`  
		Last Modified: Wed, 05 Feb 2025 23:03:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d728cbc33a1a0529f9344c632e78b243de15f5a71b791ad8491184d3c44d54`  
		Last Modified: Wed, 05 Feb 2025 23:03:24 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:fbc10ae447d60f557f46a88b4a97f8989a70725f5c10c63ec29ecceda3c4bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe02d99294c3776eb395e4cd677956f0cbfb7aead03c60c24ba9f01843b4481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 23:03:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 23:03:31 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01d6ada1f3c34476d5f663703b4434c4104e1a831deaa1b2409de5bff2ffbc`  
		Last Modified: Wed, 05 Feb 2025 23:03:32 GMT  
		Size: 1.2 MB (1245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a864e8e6eb746f10a36795c932c4a7eb97397bc384f2e3dff1e5988111848`  
		Last Modified: Wed, 05 Feb 2025 23:03:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e6436e89da58fc853fa5086bcbc6be05295037dff0c7ab576388222ff195d`  
		Last Modified: Wed, 05 Feb 2025 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1852c6fa96d530d07a157f666195024fdeaae5701aa873e7bc46ae5410d2288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e64340b1fb5c6f7bb69e69b6c5bf0858f7caf3db18ada266e3b5a291db2ea`

```dockerfile
```

-	Layers:
	-	`sha256:e01208f121e4ddbddf36c92b3408ed5bab467ac5bd516ac76461585fb5c245c3`  
		Last Modified: Wed, 05 Feb 2025 23:03:42 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c98f5e85fa5bdda0c1b8d8a70f07d88663f27980d5a44da97846e8df0fb23df`  
		Last Modified: Wed, 05 Feb 2025 23:03:43 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
