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
-	[`memcached:1.6.38`](#memcached1638)
-	[`memcached:1.6.38-alpine`](#memcached1638-alpine)
-	[`memcached:1.6.38-alpine3.21`](#memcached1638-alpine321)
-	[`memcached:1.6.38-bookworm`](#memcached1638-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.21`](#memcachedalpine321)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:bfc70df932ba629a41ab8905736976ca0721c3ce468ccd636dcf9a2845eddd68
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
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
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
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:a707bcc8ca1045fa7cea4b8e59782e7cb8ed0be2638409cd62e377b89e8e7607
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
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:bfc70df932ba629a41ab8905736976ca0721c3ce468ccd636dcf9a2845eddd68
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
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
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
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:a707bcc8ca1045fa7cea4b8e59782e7cb8ed0be2638409cd62e377b89e8e7607
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
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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

### `memcached:1.6.38` - linux; amd64

```console
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-alpine`

```console
$ docker pull memcached@sha256:a707bcc8ca1045fa7cea4b8e59782e7cb8ed0be2638409cd62e377b89e8e7607
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

### `memcached:1.6.38-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-alpine3.21`

```console
$ docker pull memcached@sha256:a707bcc8ca1045fa7cea4b8e59782e7cb8ed0be2638409cd62e377b89e8e7607
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

### `memcached:1.6.38-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-bookworm`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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

### `memcached:1.6.38-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:bfc70df932ba629a41ab8905736976ca0721c3ce468ccd636dcf9a2845eddd68
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
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
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
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:a707bcc8ca1045fa7cea4b8e59782e7cb8ed0be2638409cd62e377b89e8e7607
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
$ docker pull memcached@sha256:a84f9b06122c3e3879b0dcd1adcceb8b957356a87ae1822887882a079e827d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de2c7ee2e0fb0a7b6e022e5a088e1f85137689835280f7c50278b76ccbd91c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808b4aabc105fb7767b652e6a6d0e67cebe3731eaa91066d24e75ce2b7806ce`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c26cb971b7cc6e7426734c10cfe22cf576f19c4aca8ce643e302203d439d5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9510c5e63637fbeed0fabea0d59c2a193b85991a7328b8e4c99cfb6f4f790e`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 969.3 KB (969299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561874d971540c9ecea0d7e8b1a20949d174fef2e6ee8dd77a8ae6213ae8869`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a9de5a225dd2390caa9ce000dd8ed19a57bf52f15d7cdb905a67b20b7e14e`  
		Last Modified: Thu, 20 Mar 2025 17:58:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f8045b5787a41ae25b58a983df6a42c5b7e7e85dfbbb7c18482716723560a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb135f337b748617e1216b33a077dfb1461dd3dab6af1b561a5b1f645ca912`

```dockerfile
```

-	Layers:
	-	`sha256:59bc23819e749e5133dd78f1e5dc2b1579b1e62d7a55c95523c8fcceef921402`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76d430b6cb30c1090404f3a357cfbdfea44fa91195830e52d7a0eb634b408b5`  
		Last Modified: Thu, 20 Mar 2025 17:58:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bb083f8241faa5f51342efc4fe239ef339713786d8d09cdbdd5bcab1fdbc3d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a726de0f4b1c6db8e3cf957a6c9df0e116d427b994d2c2529d6424e6abff5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694e75f66ed3e642fdf454e0d1f95512b5554fced60f86468c8e4bd293b8f04d`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 967.7 KB (967682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f969ae37f52f2e02d95b188d045348621350dc2d69644c73127755becc93b`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a6ef04ce569f4749d12da3bab7422e3bdde9d21f4afd872732562231f135d1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:df34a36ae67a67683b2ac42d61a292a4448e3d5c666e7a0873ef52d9c6d84582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e3a4bf492a8f5762b85182e5621838d0be2b8e09731f68951923bcfc52a17a`

```dockerfile
```

-	Layers:
	-	`sha256:1cee3a766cd4da98a77d6d726d262cd2adc35297694865e0baaeb124c48a236a`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3141c4a8d2b462fc810b235284ff78eca585c2de8f96cc5f0e97f593db7826`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:119982931aeb9c567b247161541390c20b6a9bf01070dc91f9b1efbde777f294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6c4e1a64ca09fe3d941959b0fac936499b500b9f6dcf59e33ed6f95325ce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cd87818d24d55ca07beeb9b5440e0e5cd5830d7b5c893217cff3c3eb9561b`  
		Last Modified: Thu, 20 Mar 2025 17:58:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db29d7d65fe2e59533d632ee7d09f57afd1b2f91fd523fd0e5b340610e0e9`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb50b3f6ac5d05bf0703526d4a92bbc18c26d0c94617e77442565243c607e36d`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 961.4 KB (961394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297187f5fe8ebf30961721eabd6a78c4a898641e702f789918fd65514d568a6`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69083448e24dd8cf0c40c387b67822846fc504cd043eab90b225b09625d163`  
		Last Modified: Thu, 20 Mar 2025 17:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:32bf9570cf34af942b6344781ef9b8b76a7c23139e8b22884c3a73490fe519ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb9157f93d96caa57a56051684ab54a289b6e7feb25c99fcec687deb4a0f64`

```dockerfile
```

-	Layers:
	-	`sha256:718829dd2400a75a735be4709542aa498a6e1343211a0c6276b1c01c2a2edc5e`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfb79584f449f7729441469d4cbdd87b2b75bd30770b5a9bf873125fdf9ab`  
		Last Modified: Thu, 20 Mar 2025 17:58:26 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:8879fd21aee697b1abe0df94ef3b1cd454e8eae4913895bad95a4b13648fbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514169735cfd12766f9b6765abd65c4e78a49ead532126c2c5a9f32be801592`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854bdd3cff75df3780d15d25a4a7581bdf449ae742abd1e342b01aace8ae803`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 1.0 MB (1008513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6899976abb25cd4a633ba2d5a2f7df071d733546e4a92de28add0726a6dbf86`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452be3e8178b390a4b6f4fc5413fe5febd97839451d21ce530238860a248805`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f79473758a05f54e050495f89c03d4a660099e849719bb2fb6afddb3f4965eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6930a74200f7bde4852b5408ff214da6abbe8c2a81854f472c090af7dce9522f`

```dockerfile
```

-	Layers:
	-	`sha256:757b1cdede08593bdfb71ce62f994c9a292b679bc1f7a44783aa3d032224b491`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0335ab893e2aa595c0aefbb6d507e4a99b256481e5b7bd54b83b4c307473a8`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:f44b381e60dc46d0348fd04683b3c7d0c51342159567ca178e08e3eca68eabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b641465837a5e7e2c9208cd7adc6b847b179427cbe7e55efad52a99c4900435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b57e44bf61fb4cddd1e698c24d8e904b5ab14d3ccc07fdaf469a929b33134`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 988.6 KB (988634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a75df29eb4a9d0acb7c523ac28dd718a522b03f6598660f4e7713db8ea506`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41539a4259c4ff3e390778ef767ede7a06952a8c17136239ec7a3d5d5ab57a2`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:cf44b65bbe91e1430e4788bc77324ba7883e0c1dd2165165092695bdba778bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadf5362b4eb2f0421720ff81563b57976a1b3522f005b1fdbd25b9ec7d8eaac`

```dockerfile
```

-	Layers:
	-	`sha256:6145dd52778d1f668e6a0bc785ae5a92c33446092836533139863f3254f2fdea`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b64fbfba36ad744930ea5d9b77ee42887a48e16dd43e02a9c2c3a4049f86cc6`  
		Last Modified: Thu, 20 Mar 2025 18:06:39 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:634e789639c5d7ec82c7bc06d865eb88e40ad421ffc4ea5aa010b0e62050c9fc
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
$ docker pull memcached@sha256:3f93f07696abe4f2408661428e989c9280b2c57e175de4ffdf0da2296f2695ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9abf7224d37ad13efab8a858c96c9aac162efdf12bb085bff25ae6cf3266f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d0ecc567f74906a5676050245f6c9cd1a12750f83c9d6fceee16a02dd1c25`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c07924b984463d8d6b92da577c082a8cd10a316b62f4b851729f71565d581f7`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbae4e0f065d27c0a0bb7e4214175f4cabb054c9aa57737290fb391bc074540`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 1.3 MB (1267515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a13cedb43d44e4da32176047ec198250434e2f1faf36f1e6d02aba8c195ebe`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b6471521ce0467c0388272b14ce271a0c2528f3a1478d3026603931ae91e0`  
		Last Modified: Thu, 20 Mar 2025 17:58:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:dcdee278e8ce6ef8092dc3999e45e2247114e06ffff75bc6f0ff3e31226733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67497a34cb7487cd919f1e4ba1503b162fb8481208e9d807ba83a2b861d75d7`

```dockerfile
```

-	Layers:
	-	`sha256:0ff2a89f83039021ac88d6e8399d14ac3ca2806df547024277f562b301f4f3ac`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb53ca79537d1e2e402fed021ebee753089f0067d4e681d3bb216cc702291f5`  
		Last Modified: Thu, 20 Mar 2025 17:58:09 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:672a9625711d93ae840847c7595d2eb39b7fceb0d8017ed94e33936c6ba880e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc49b2d1d511d9f99c06cd95133336981d56578c2b21631fec0d9805cf462bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bec25cf1e7a193578843814fd91bdbfb75fe09d0722c1d31af0ff55c638895`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c810700a47b11313e37edd85492aee921c43806e7a107d9bfe2f62513238ae`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e54755f777236c31b9a66d864c49bbd0d6f7cc1c27e92ffbcdf76bb5b3f6c0`  
		Last Modified: Thu, 20 Mar 2025 17:59:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:17a228a3305fd7b53c9d58e35aafd04637376fb654778aa512720f76a12cfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d89468039e6f5eb51aedd757b083a5824de88a72c362469fe26b02fc03f813`

```dockerfile
```

-	Layers:
	-	`sha256:57691bd1c158ada3391a88ad8ab27a5497a8b6f3a021a12e4b65d10d8f6638d8`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b9acd4c796be0c3c0e0f1c6f580b031d52e421db5757d90af64841963146f`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:11e45001b145f2e3cf612988ccf6729d474c4a0166979636b0bbb22da1d96ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cfd079ffc7d9602439311a2ed920a5fcf1d2fc39182883d32a1026f129e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035bc2b5de12b342aaa584bf3a00c6b80146da9ba6172f848a9c0c66498ad39`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38079955333499011756e496a625ed7fe4599b4bba1ed27c648b5693f61e9b4`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0635351590aed437040b58c7ab49b6cb431b31b441e37c6a3f268c16fd1c62f`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 1.3 MB (1266510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f7ad4641384f395e335ddf193eedd46c241fe134ce9d637dc875e94b643db`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67732a5f082a6c459c0b1dc629b6daf8908c46234a7bf9ef599e2deeeccf4699`  
		Last Modified: Thu, 20 Mar 2025 17:58:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b1e381fb5b8350aea7167ae0a68b91a56265a69511d3030816358b3b5c504655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37076c65cdf913cc4c1102c31c4dc5310d4fbe0ec6e5d13da78a399a0a429633`

```dockerfile
```

-	Layers:
	-	`sha256:9fb102dc0074ea8c78b3d69e4c7055309e3827e8ed0937a40280afdc8c7b1760`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1042f9f0a63298cfd9fc927451bcb7b7343cbaa3b8e9e1483fb22ca6c1c82`  
		Last Modified: Thu, 20 Mar 2025 17:58:22 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:1e7b338c56b75ad262c10d14c9993d62a944da874e97fb632ae2bcb228186f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31695612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c18996a55f345ee83a5df64d94865eae2fa85f4ecd17fe287ca3701478c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cdc546fd3b4030452d480047754123bf9945b94bae09c45ceaf3acb8d0a344`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad193b9bc4ccf2fb4bbd4169f62c6ff4a601656b9ba2316f3e5ef47208edc9`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b836e465ed07e2090b84f391b8b2f58920fb72d5960aadcc283cd4c7d21`  
		Last Modified: Thu, 20 Mar 2025 18:10:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a5801f12d46d55715db6879f56ece89398d3ecbccd3dfdcb6ecf442afb508dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09ee3dffbc3baabafe075154d8ca3f790cce51a1373b56408c001e65eafb6f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb1d6c862df2913a9d507f7507f581c903ba76b24e87205849756f55ee60be`  
		Last Modified: Thu, 20 Mar 2025 18:10:02 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:532dba1ca785f04bdc4813c498ed31536beb745ec689100cb035d6fa05bb88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9010ebcd6e0a9afc8e4dd54e764700cf212dae5898e0d6ea83005d1f7ce9b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a560ec2e503c42f745525c374418b2a9bd57b9369c77c84b77d45754c6092b`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.3 MB (1332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f409af03b3a0f71e5a5fe610b530665ed60915f4cbd9e6fe791ae78a9ec2`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313175e9a170bc0c080e47851a6511ea6a19d78721ad9f68bf606e2b830f19e`  
		Last Modified: Thu, 20 Mar 2025 17:59:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a3892339dc3d8c9995b03c00ad458952d78ec3d292ac466f64e53319c264e9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924699269333d1c93f4187f9e1663df847ced1d0be37ced64ea1df175a74e69b`

```dockerfile
```

-	Layers:
	-	`sha256:e6c6cc854af470ea8c6f48928607cd5f30eab0f29e28c8bda159382cd9a1ff18`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cadc546fe38b1d30483815f3979481b7cbaf4b05be897e101d497c351e220c`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:af6a399bb3bcdd5d9215e3525acee3b072350e8ab726d632ccdf96a4f16c1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4232f274a4db237d45fc5fb9d3735ca39214fc071860e8a1d1333d3a9fdbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a29a8b075e125d5b7bdaf62129aeae11317632e6f4a04eb87b67f4f3201353`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.2 MB (1245456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc23045db3c49bbabbd17e864e2c796ae368ff94b959d969395fa975155f84`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8551d4cee6ae75528101d67e05db27075495a2cc45e9871f2ade6dbd210eaf9`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e3fccf65b8a51eddbf2f9bcc52989eb8741acde3e83d7a178ce7f222a60dfa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33782eb38bfa13dbdf4430755ca9e2f90e517f94823e278b7cbfa1dec5f26a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b7de4dad4869158b36c6a8abb2fee99b0061806ca2f3b3b01b7bcf32797b107`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ffb6e605342bb89a7d9a64321537af2b01267d4709ea2bcc80977cc2d34780`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
